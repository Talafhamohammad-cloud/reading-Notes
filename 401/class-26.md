# Permissions:
***Together with authentication and throttling, permissions determine whether a request should be granted or denied access.***
***Permission checks are always run at the very start of the view, before any other code is allowed to proceed. Permission checks will typically use the authentication information in the request.user and request.auth properties to determine if the incoming request should be permitted.***
***Permissions are used to grant or deny access for different classes of users to different parts of the API.***
***The simplest style of permission would be to allow access to any authenticated user, and deny access to any unauthenticated user. This corresponds to the IsAuthenticated class in REST framework.***
***A slightly less strict style of permission would be to allow full access to authenticated users, but allow read-only access to unauthenticated users. This corresponds to the IsAuthenticatedOrReadOnly class in REST framework.***

##################################

## How permissions are determined?
Permissions in REST framework are always defined as a list of permission classes.
Before running the main body of the view each permission in the list is checked. If any permission check fails an exceptions.PermissionDenied or exceptions.NotAuthenticated exception will be raised, and the main body of the view will not run.

**When the permissions checks fail either a "403 Forbidden" or a "401 Unauthorized" response will be returned, according to the following rules:**

1-The request was successfully authenticated, but permission was denied. — An HTTP 403 Forbidden response will be returned.

2-The request was not successfully authenticated, and the highest priority authentication class does not use WWW-Authenticate headers. — An HTTP 403 Forbidden response will be returned.

3-The request was not successfully authenticated, and the highest priority authentication class does use WWW-Authenticate headers. — An HTTP 401 Unauthorized response, with an appropriate WWW-Authenticate header will be returned.

##################################

## API Reference:
1-AllowAny The AllowAny permission class will allow unrestricted access, regardless of if the request was authenticated or unauthenticated.

2-This permission is not strictly required, since you can achieve the same result by using an empty list or tuple for the permissions setting, but you may find it useful to specify this class because it makes the intention explicit.

    2.1-IsAuthenticated The IsAuthenticated permission class will deny permission to any unauthenticated user, and allow permission otherwise.

3-This permission is suitable if you want your API to only be accessible to registered users.

    3.1-IsAdminUser The IsAdminUser permission class will deny permission to any user, unless user.is_staff is - True in which case permission will be allowed.

4-This permission is suitable if you want your API to only be accessible to a subset of trusted administrators.

    4.1-IsAuthenticatedOrReadOnly The IsAuthenticatedOrReadOnly will allow authenticated users to perform any - - request. Requests for unauthorised users will only be permitted if the request method is one of the “safe” methods; GET, HEAD or OPTIONS.

5-This permission is suitable if you want to your API to allow read permissions to anonymous users, and only allow write permissions to authenticated users.

##################################

## DjangoModelPermissions:

1- This permission class ties into Django’s standard django.contrib.auth model permissions.

2- This permission must only be applied to views that have a .queryset property or get_queryset() method.

3- Authorization will only be granted if the user is authenticated and has the relevant model permissions assigned.

4- POST requests require the user to have the add permission on the model.

5- PUT and PATCH requests require the user to have the change permission on the model.

6- DELETE requests require the user to have the delete permission on the model.
