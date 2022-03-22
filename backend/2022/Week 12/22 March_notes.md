```js
const response = fetch("http://get-some-data.com/", {
    method: "POST", // default
    headers: {

    }
})
    .then(() => {

    });


const axiosResponse = axios.post("http://get-some-data.com/", {
    headers: {}
});
```

## Servers

When you send a REQUEST to a server, you expect a RESPONSE

## Http vs Https

Information sent over Http is UNSECURED and can be ready by anyone snooping into the traffic

Https (s meaning secure) is encrypted traffic

SSL certificate is needed for https traffic

[https://www.openssl.org/](https://www.openssl.org/)

# Port numbers

Here is a domain;

http://localhost:1948/something/backend-overview.md

PROTOCOL: http://
HOST: localhost
PATH: something
PORT: :1948 _This is not normal_

By default all HTTP web traffic comes over port 80
By default all HTTPS web traffic comes over port 443


# Express

```js
// here is an endpoint
// / means root
// here get is the request type
app.get("/", (request, response) => {

    // request is an object
    // response is an object
    console.log("Request received! 🥸");
});
```

## Request

The **request** object contains everything to do with the request, headers, body

## Response

Be very careful with `response.send`! Why? Because only 1 of these is allowed to run in the function.

You can use `return` to halt the function from running


# breaking down a URL with query parameters

https://api.openweathermap.org/data/2.5/weather?lat=35&lon=139&appid={API key}

PROTOCOL: https://
HOST: api.openweathermap.org
PATH: /data/2.5/weather
QUERY PARAMETERS: ? lat=35 & lon=139 & appid=89834iadhfiadr24

? = what comes next, is a list of query parameters
& = we are attaching a new query parameter
everything else, are just keys and values

# Parameters

- query parameters (optional)
- request parameters (part of the path)


