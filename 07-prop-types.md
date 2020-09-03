# Validate Custom React Component Props with PropTypes

Consider this example:
```jsx
const element = <SayHello firstName={false} />    // give the boolean value to firstName

function SayHello({firstName, lastName}) {
  return (
    <div>Hello {firstName {lastName}!</div>
  );
}

ReactDOM.render(element, querySelector('#root');
```

`propsType` is allowed to add runtime validation of the props passed to components.
`propsType` validate the types of props that being passed when render.

```jsx
SayHello.propTypes = {
  firstName(props, propName, componentName) {
    if (typeof props[propName] !== 'string') {
      return new Error(
        `Your error message.`
      );
    }
  }
}
```
