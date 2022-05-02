# DRY

Don't repeat yourself

Why do we want to avoid repetition?

- repetition leads to redundancy
- higher maintenance cost
- can lead to anomalies with our data
- which "copy" is the correct one?

# Single source of truth

https://en.wikipedia.org/wiki/Single_source_of_truth

# A note on Schema Validation

Schema validation is **only** used through the application we build

If we use another tool like MongoDB compass or Altas web interface to change or add data - this does not involve our schema validation

# Creating references

When we create a reference from one collection to another, we are creating a one way relationship between those collections

How?

1. Set the datatype to `ObjectId`
2. Give the reference to the collection I am trying to refer to

# Types of relationships

one-to-one relationship - where **one document** in collection A refers to **one document** in collection B

##### Example
```
userId: ObjectId("4867jhf4jfg948393493495344")
```

one-to-many relationship - where **one document** in collection A refers to **many documents** in collection B

##### Example
```
reviewId: [
    ObjectId("4867jhf4jfg948393443495344"),
    ObjectId("347jhf4jfg94d8393443495344"),
    ObjectId("7767jhf4jfg948393443495344"),
]
```

# Populating references

A reference consists of an ObjectId, which is not really useful to us (or to the client)

We can use the `populate()` method to "look-up" the data behind that ID

https://mongoosejs.com/docs/populate.html

# Security

We can use the `select()` method to choose which fields we would like to return

Select expects a list of strings (one string per key)

We can use the `-` symbol to remove a key

# Diagrams

## Creating relationships with references

![References-relationships](./MongoDB%20references-references.drawio.png)

## Data without references

![Data without references](./MongoDB%20references-without%20references.drawio.png)
