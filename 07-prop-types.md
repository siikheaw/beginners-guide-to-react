# Validate Custom React Component Props with PropTypes

When you create reusable React components. You want to make sure that people use them correctly. The best way to do this is to use TypeScript in your codebase to give you compile-time checking of your code.

If you're not using TypeScript, you can still use PropTypes to get runtime validation.

```jsx
const element = <SayHello firstName={false} />    // give the boolean value to firstName

function SayHello({firstName, lastName}) {
  return (
    <div>Hello {firstName} {lastName}!</div>
  );
}

ReactDOM.render(element, querySelector('#root');
```

`propTypes` validate the types of props that being passed when render.

```jsx
SayHello.propTypes = {
  firstName(props, propName, componentName) {
    if (typeof props[propName] !== 'string') {
      return new Error(
        `The component ${componentName} nees the prop ${propName}` to be a string, but passed a ${typeof props[propName]})
      );
    }
  }
}
```
