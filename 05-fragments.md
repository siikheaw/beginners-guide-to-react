# Render two elements side-by-side with React Fragments

Normally, in React, we cannot create sibling side by side like in HTML:
```html
<span>Hello</span>
<span>World!</span>
```

In React this doesn't work:
```jsx
// Error
const helloElement = React.createElement('span', null, 'Hello');
const worldElement = Raect.createElement('span', null' 'World!');
ReactDOM.render(helloElement, worldElement, document.querySelector('#root'); // Error
```

However, React has `React.Fragment` to solve this problem:
```jsx
const helloElement = React.createElement('span', null, 'Hello');
const worldElement = Raect.createElement('span', null' 'World!');
const element = React.createElement(
  React.Fragment,
  null,
  helloElement,
  ' ',
  worldElement
);
ReactDOM.render(element, document.querySelector('#root');
```

And even easier with JSX:
```jsx
const element = (
  <React.Fragment>
    <span>Hello</span> <span>World!</span>
  </React.Fragment>
);
```

JSX has a special syntax for `React.Fragment`:
```jsx
<>
  <span>Hello</span> <span>World!</span>
</>
```

---

## Recap
- Normally, we can't create sibling side by side in React. But `React.Fragment` 
