# Context API

Is all about storing information, and making that information available to your application

Similar to `useState` - except `useState` creates a local state which is only available to that component

## What problem does Context API solve?

It helps to avoid "prop-drilling" - where we may pass a prop down multiple levels in the hierarchy

Prop-drilling - this is a code smell!

> What is a [code smell](https://refactoring.guru/refactoring/smells)?
> These are coding issues that are well known

## Context, Context Provider and Context Consumer

### Context

We create the context using the `createContext` function, then;

### Context provider

provides the information

We use the `value` attribute to share data with our context

### Context consumer

uses the information

1) We have to import the context
2) use the `useContext` hook - with the imported context as an argument

## You can have multiple contexts in your application - each context will have its own purpose

> For example
> 1 context for login information - username, JWT, user_id
> 1 context for theme, font size, day theme / night theme

Don't use Context API - unless you really need to!

> KISS = Keep it simple, stupid! Keep it stupid simple! - Don't overcomplicate things, if you don't need to
> DRY = Don't repeat yourself

## Patterns / anti-patterns

A pattern is an established way of doing things / an established practise. (usually) no controversy around a pattern

Anti-pattern - it's a recognised _bad_ way of doing things

## React attribute "children"

"children" is a reserved attribute / prop which ALL components have

```js

function Text({ children }) {
    return (
        <>
            {children}
        </>
    )
}
```

If you want to render the `children`, first destructure or grab from the props the `children` prop,

then render using `{childen}`

![The tree](./Context%20API-The%20tree.drawio.png)

![Bad example](./Context%20API-With%20Context%20API%20-%20bad.drawio.png)

![Good example](./Context%20API-With%20Context%20API%20-%20good.drawio.png)

![Common example](./Context%20API-Common%20example.drawio.png)