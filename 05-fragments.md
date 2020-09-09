# Render two elements side-by-side with React Fragments

In React, you can't render two React elements side-by-side. They have to be wrapped in another element (like a `<div>`).
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

React Fragments let you group a list of children without adding extra nodes to the DOM. Using the React Fragments API:
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

You can also use a React Fragments Element:
```jsx
const element = (
  <React.Fragment>
    <span>Hello</span> <span>World!</span>
  </React.Fragment>
);
```

Since React Fragments is so common, JSX has a **special syntax** for it:
```jsx
<>
  <span>Hello</span> <span>World!</span>
</>
```

---

## Recap
- Normally, we can't create sibling side by side in React. But with `React.Fragment` make it possible.
- Two way to use `React.Fragment`
  - `<React.Fragment></React.Fragment>`
  - `<></>`
