# Create a Simple Reusable React Component

Consider this example:
```jsx
const message = <div className="message">Hello World!</div>
const element = (
  <div className="container">
    {message} // -> Hello World!
    {message} // -> Hello World!
  </div>
);
```

What if we need to display a different message in JavaScript, we create a function:
```jsx
const message = (props) => <div className="message">{props.msg}</div>
const element = (
  <div className="container">
    {message({msg: 'Hello World!})}
    {message({msg: 'I am React!})}
  </div>
);
```

In JSX:
```jsx

```

## Note
In JSX, if we try to create a component with no-capital letter like `<message>`, React will warn you and treat this as a string:
```jsx
// DON'T do this!
<message>Hello World!</message>

// Will compiled to:
React.createElement("message", null, "Hello World!)
```

To create a component in React, use a capital letter:
```jsx

```
