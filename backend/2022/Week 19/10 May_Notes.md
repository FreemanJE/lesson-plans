

## Responsibility

Every function should have 1 responsibility

## multer

```
npm i multer
```

- middleware
- works with form data
- images are given a unique name

### configuration

We can use it to save a **file** or **multiples files** from a request object

- each request can only be configured to handle either a single file or multiple files
- you can configure the **frontend** to handle specific types of files
- can also configure it to reject files above a certain
- you can choose a file size limit
- you can also configure where to store the file on the server



## Uploading on frontend

We can use MIME type to force the frontend to allow only certain types

