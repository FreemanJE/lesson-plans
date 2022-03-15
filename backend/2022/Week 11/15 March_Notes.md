# Environments

A place where our code is run

We are going to be talking about 2 environments;

1. Browser (frontend)
2. Node.js (backend)

# Modules in backend

Node.js prefers to use the Common JS approach to importing and exporting modules

```js
// Common JS approach
const colors = require("colors");
```

We can tell Node.js to use ES6 module by either;

1. Renaming our files with the `.mjs` extension
2. Adding to our `package.json`;

```json
{ "type": "module" }
```

# Node.js environment variables

`process` object can be read anywhere within your node application - accessible from anywhere

No need to import `process`, it is available everywhere

- `process.argv` gives us access to the command line arguments
- `process.env` - we can use the `dotenv` package to add keys from our `.env` files

# .gitignore

Always remember to add `.env` to your `.gitignore` file!

# Other resources

https://github.com/DCI-TechEd/glossary
https://www.electronjs.org/
https://reactnative.dev/
https://github.com/webpro/reveal-md
