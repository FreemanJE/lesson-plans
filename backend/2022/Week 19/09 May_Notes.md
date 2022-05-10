## http and https

### http

- http is vulverable to the **man in the middle attack**
- http is not secure
- information is sent in plain text over http

### https (secure http)
- information is encrypted

https://letsencrypt.org/

TLS is a more updated form of SSL

## Session based auth vs JWT auth

### Sessions

- Sessions are handled by the server
- created on the server
- Stored on the server
    - very secure!
    - really bad for resource usage
    - not portable
- validated by the server

### JWT

- Created on the server
- Stored on the client
    - less impact on server resources!
    - more vulnerable to attacks (because it's stored on the client)
- validated by the server

## Authorisation


```javascript

router.patch("/user", async(req, res) => {
    // update the user document
}

```

What do we need to ensure that the user can perform the above action?

1. If the user does not have a token, we will redirect them to the login
2. We need to validate their token
    - has the token been tampered with?
    - Has the token expired?
    - Does the userid (stored in the token) exist?


## Passwords and hashing

- What is salt?

Add a random string to the password before we hash it

## http status codes

https://www.npmjs.com/package/http-status-codes


