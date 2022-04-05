## Technology stack

The course you've been doing at DCI is the MERN stack

MongoDB
Express
React
Node

## MongoDB


Also known as a NoSQL database = not SQL

SQL stores information via relations between data

NoSQL stores flat , JSON like (BSON) documents

We can use MongoDB Compass to connect to our database, but it is not necessary


## Inside a MongoDB Database

**Database** contains **Collections**

A **collection** is _like_ an array of information

A **collection** contains **Documents**

A **document** is _like_ a JS object

```js
// This is not a MongoDB collection! Just it works in a similar way
const users = [
    {
        id: "839jfv934v9345",
        name: "Random Name 1",
        email: "random1@Random.com"
    },
    {
        id: "449jfv934v93545",
        name: "Random Name 2",
        email: "random2@Random.com"
    },
    {
        id: "559jfv934v93545",
        name: "Random Name 3",
        email: "random3@Random.com"
    }
];

// This is not a MongoDB collection! Just it works in a similar way
const products = [
    {
        name: "Guitar",
        stock: 345,
        imgUrl: "/path/guitar.png"
    }
];
```

## Validation and Schemas

firstname: "Random Name 3",
lastname: "Last name"
email: "random3@Random.com"
