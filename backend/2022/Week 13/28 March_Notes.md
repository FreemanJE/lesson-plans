# What is an endpoint?

It is an address to a digital resource, for example, this URL:

http://localhost:3001/planets/find/Mars

Is the endpoint for a planet search

# URL params or parameters

2 types;

1. Request parameters - these are not optional, we must include them in the URL

    > http://localhost:3001/planets/find/Mars

    Here, "Mars" is the request parameter

2. Query parameters - these are optional, they have a key / value relationship


    > http://localhost:3001/planets/find?name=Mars&size=58

    Here, "Mars" is the query parameter


# Response object

By default, response code will be 200 unless you change it


`response.send`

- will look at the datatype of the information you are trying to send
and try and conform the response to match the datatype
- sends a response

`response.json`
- will expect JSON as the datatype
- sends a response

# Method chaining

Some objects (not all!) will allow us to chain methods together, for example `response`


# Function returns

If no return statement is included in the function, then the function will automatically return `undefined`

# Application routing

Why?

- We can reduce repetitive pathnames - we can reduce the potential for errors
- We can simplify our codebase

# Middleware

Just a function that sits in between the request being received from the client and before the response is sent back to the client

We can use that middlware anywhere in that chain

Order of the middleware is really important!


## Invoking middleware

There are many different ways of invoking it into our application;

1) `app.use(genericMiddleware)`
2) `app.use("/satellite", genericMiddleware, satelliteRouter);`

## Invoking multiple middlewares

1. Here both middlewares will only run before the `/planet` route

```js
app.use("/satellite", satelliteRouter);

app.use(genericMiddleware);
app.use(genericMiddleware2);

app.use("/planet", planetRouter);
```

2. `app.use("/planet", genericMiddleware, genericMiddleware2, planetRouter);`

3. `app.use("/planet", [genericMiddleware, genericMiddleware2], planetRouter);`

4.

```js
router.use(genericMiddleware);
router.use(genericMiddleware2);
```

