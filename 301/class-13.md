# In your own words, describe what each group of status code represents:

**100’s =**tell the client that the header part of the request has been received and the server will try to comply with a transmission demand of the client.

**200’s =**tell the client that its request was accepted. In case of asynchronous processing of a request (202), this doesn’t mean the request was successfully processed only that it met all validation requirements at the time of sending

**300’s =**tell the client that its request was accepted. In case of asynchronous processing of a request (202), this doesn’t mean the request was successfully processed only that it met all validation requirements at the time of sending

**400’s =**These are the client error codes

**500’s =**Often they indicate problems with overwhelmed servers or unreachable servers behind proxies, but sometimes they can be directly related to client requests that trigger error exceptions on the server.

# What is a status code 202?

Accepted - Often used for asynchronous processing. This code tells the client that the request was valid, but its processing will finish sometime in the future. The response body should include an URL to the finished resource with some information about when it will be available, or an URL to some monitoring endpoint that tells the client when the resource is available.

# What is a status code 308?

Permanent Redirect - This tells the client to use another URL to access the resource and not use the current URL anymore. It’s helpful when we have multiple endpoints for one resource, but don’t want to implement reading from all of them

# What code would you use if an update didn’t return data to a client?
204 No Content

# What code would you use if a resource used to exist but no longer does?
202 Accepted

# What is the ‘Forbidden’ status code?
403 Forbidden: The client has authorized or doesn’t need to authorize itself, but still has no permissions to access the resource.

Build A REST API With Node.js, Express, & MongoDB
Build A REST API With Node.js, Express, & MongoDB

# Why do we need to pull our MongoDB database string out of our server and put it into our .env?
in order to deploy our application we need it not local host

# What is middleware?
it mean to pass to router portional express in the subiscriber file, to get us the router from express

# What does app.use(express.json()) do?
to make our server accept JOSN as a bode insted of a post element

# What does the /:id mean in a route?
every thing has this url or after it will go into the subiscriber Router

# What does a 500 error status code mean?
means Internal Server Error, which can be anything from a missing header field the backend accessed without checking its existence to an unreachable third party service the backend wanted to call.

# What is the difference between a status 200 and a status 201?
200 OK- :Most of the read actions will be answered with a 200 OK status.
202 Accepted : If the update is done asynchronous, this code can be used. It should include an URL to access the updated resource or an URL to check if the update has been succeeded. It can also include an estimation of how long the update will take.