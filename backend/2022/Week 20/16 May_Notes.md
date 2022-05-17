## Storing JWT in frontend

### localStorage/ sessionStorage

Pros:

- easy to access (from frontend)

Cons:

- not secure. Why?

A compromised website can read the contents of this storage - all a hacker needs is a copy of the token to impersonate you

### httpOnly cookies

Normal cookies have the same problems as localStorage / sessionStorage

Requires co-ordination between frontend and backend

- backend - we must send a httpOnly cookie

```
response.cookie("jwt", token, {
    httpOnly: true,
    secure: false, // we are not using https
    sameSite: "lax",
})
```

- frontend - we must pass the credentials option


##### axios
```
{
    withCredentials: true,
}
```

## Security

To be extra secure you should;

- use https
- want to be using the same domain for backend / frontend
