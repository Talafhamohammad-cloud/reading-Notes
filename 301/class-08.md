# What does REST stand for?

REST is an architectural style for building distributed systems based on hypermedia.

REST is independent of any underlying protocol and is not necessarily tied to HTTP.

Most common REST API implementations use HTTP as the application protocol, and this guide focuses on designing REST APIs for HTTP.

## REST APIs are designed around resources,

 which are any kind of object, data, or service that can be accessed by the client.

## What is an identifer of a resource? Give an example.

A resource has an identifier, which is a URI that uniquely identifies that resource. For example, the URI for a particular customer order might be:

https://adventure-works.com/orders/1

## What are the most common HTTP verbs?

GET retrieves a representation of the resource at the specified URI. The body of the response message contains the details of the requested resource.

POST creates a new resource at the specified URI. The body of the request message provides the details of the new resource. Note that POST can also be used to trigger operations that don't actually create resources.

PUT either creates or replaces the resource at the specified URI. The body of the request message specifies the resource to be created or updated.

PATCH performs a partial update of a resource. The request body specifies the set of changes to apply to the resource.

DELETE removes the resource at the specified URI.

## What should the URIs be based on?

Adopt a consistent naming convention in URIs, , it helps to use plural nouns for URIs that reference collections. It's a good practice to organize URIs for collections and items into a hierarchy.

## Give an example of a good URI.

example.com/articles/good-uri-design.

## What does it mean to have a ‘chatty’ web API? Is this a good or a bad thing?

web APIs that expose a large number of small resources.

## What status code does a successful GET request return?

A successful GET method typically returns HTTP status code 200 (OK).

## What status code does an unsuccessful GET request return?

If the resource cannot be found, the method should return 404 (Not Found).

## What status code does a successful POST request return?

If a POST method creates a new resource, it returns HTTP status code 201 (Created).

## What status code does a successful DELETE request return?

If the delete operation is successful, the web server should respond with HTTP status code 204.
## How would you match your name using RegEx?

^[a-zA-Z'-]+$
where 
### ^ means start of the string, and $ means end of the string.
### […] is a character class which anything inside it will be matched.
### x+ means the pattern before it can be repeated once or more.

## nside the character class,

### a-z and A-Z are the lower and upper case alphabets,
### ' is the apostrophe, and
### - is the hyphen. The hyphen must appear at the beginning or the end to avoid confusion with the range separator as in a-z.