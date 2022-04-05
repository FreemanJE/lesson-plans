## Creating documents inside our collection

- When we create a new document, MongoDB **automatically** creates an **_id** field for that document
- We can use that **id** to uniquely identify that particular document for that collection


### How?

- We can use MongoDB Compass tool / MongoDB Cloud database interactive tool

**WARNING!**

When we use the above tools, there is no validation of our data!

### How to validate?

- We will use the mongoose library!
- We will use schemas

```
npm i install
```

### Mongoose

- Mongoose relies heavily on promises

### What are schemas?

- Validates the data we want to store in our collection
- Validates the `fields` - invalid keys will NOT be included
- Validates the datatypes - `string` is a `string`, a `number` is a `number`

### Extra validation

required && default

### What happens if you change your schema after adding data?

- The old data will not match the new schema
- In a real life scenario you would have to perform "data migration" on the old data
- A developer would have to build a tool to **migrate** the old data to the new data - every single document has to be updated

### What happens if you create the data multiple times?

- MongoDB will add the data multiple times
- It is possible to write some code to prevent this from happening

### Models

- Schemas do not do anything on their own
- We need to pair them with a model, in order make them functional
- A model reflects a **collection** - it is the connection to the **collection**


### Model methods

- `create` creates new data
- `find` read data

## Promises

```js
  Guitars.create({
    name: "G&L",
    stock: 200,
    imageUrl: "",
    price: 3494,
  })
    .then(() => {
        console.log("product created");
    })
    .error(() => {
        console.log("error");
    }
```

Nesting can be a problem, so we use `async/ await`


## Handling errors

```js
app.post("/", async (req, res) => {
  try {
    await Guitars.create(req.body);
  } catch (error) {
    return res.status(400).send("Error");
  }

  // 1. make the server handle errors gracefully (not crashing)
  // 2. inform the user that their data was invalid?
  res.send("ok");
});
```
