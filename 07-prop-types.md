# Validate Custom React Component Props with PropTypes

```jsx
const element = <SayHello firstName={false} />

function SayHello({firstName, lastName}) {
  return (
    <div>Hello {firstName {lastName}!</div>
  );
}

ReactDOM.render(element, querySelector('#root');
```
