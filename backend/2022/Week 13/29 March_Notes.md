
# Middleware

Use `express.json()` middleware to inform express that the request can include json body

> DO NOT USE `body-parser` <

## express-validator

https://express-validator.github.io/docs/validation-chain-api.html

Sanitize **before** you validate!

## Writing our middleware

`app.use()` expects middleware

- Middleware has quite a lot of power
- Can do anything from processing information from the request object, to
- kicking the user off the request-response cycle

# Why would we use asynchronous operations (promises?)

- we can have commands _sort of_ running at the same time, rather than one after the other
- Research: event loop

await - makes promises synchronous

# Validation and sanitisation

E-mail addresses follow a set of rules

franco@franco.com ✅
franco@franco@.com ❌

If you try to send an e-mail to `franco@franco@.com` you will get an error

# **YOU CAN NOT TRUST THE CLIENT!**

Why?

- Users are fallible; they can make mistakes (spelling errors, etc)
- Browsers are an "open system" - bad users can modify the data which is being sent from the browser
- The client can disable javascript! - any js validation you try and do in the client can be defeated
