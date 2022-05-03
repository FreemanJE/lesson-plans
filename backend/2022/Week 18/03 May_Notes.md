## why use cors package?

cors = cross-origin-security-policy

These two domains are not the same because of same-origin-security-policy;

http://localhost:3000
http://localhost:3001

## http status codes

https://www.npmjs.com/package/http-status-codes

## Development vs. Production

- Development

The version of the application (frontend or backend) which is currently being developed

(usually) a lot slower
includes debugging information

With create-react-app, you can run the development version with

```bash
npm start
```

- Production

The final release of an application
The version you would deploy to a web server
- JS, CSS, HTML minified

```bash
npm run build
```

# React

## useEffect hook

We use this hook to create side effects within our component

[] = empty array means - run after the component has mounted and rendered

## Array.map()

The map method is a transformation method

We transform from one array to another

With React, we transform from raw JSON array to an array of React elements

##### React component lifecycle

![React component lifecycle](./React%20Component%20Lifecycle.drawio.png)

##### useEffect hooks

![useEffect hooks](./useEffect%20hook%20within%20a%20component.drawio.png)

##### Using Array.map() in React

![Using Array.map() in React](./Using%20Array.map()%20in%20React.drawio.png)