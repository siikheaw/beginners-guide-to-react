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
const Message = (props) => <div className="message">{props.msg}</div>
const element = (
  <div className="container">
    <Message msg="Hello World!" />
    <Message msg="I am React!" />
  </div>
);

// Or using props.children
const Message = (props) => <div className="message">{props.children}</div>
const element = (
  <div className="container">
    <Message>Hello World!</Message>
    <Message>I am React!</Message>
  </div>
);
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
<Message>Hello World!</Message>

// Will compiled to:
React.createElement(Message, null, "Hello World!">
```

---

## Recap
- To reuse code, we create own custom function components which accept `props` object and return more React components.
- Components must start with a capital letter. So that Babel can compile to pass the function itself to React.createElement rather than the string message to React.createElement.
