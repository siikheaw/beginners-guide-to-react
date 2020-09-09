# Create a User Interface with React's createElement API

React uses the same APIs to control and update the DOM that we did in the previous lesson. But it offers so much to the table that we're going to introduce it into the project and rewrite what we've written to React code. Instead of creating DOM elements, we'll create React elements and then hand those off to `react-dom` to handle turning those into DOM elements and putting them into the page.

If you're ever learned or used React before, you're probably more familiar with JSX than React's `createElement` API, but it's important to understand the `createElement` API first.

With React, we can create element using React's createElement API:
```js
const element = React.createElement(            // create an element with `React.createElement`
  'div' {                                       // element
  children: 'Hello World!',                     // props.children
  className: 'container'                        // props.children
});
```

Full code:
```html
<div id="root"></div>
<!-- Get React from UNPKG -->
<script src="https://unpkg.com/react@16.12.0/umd/react.development.js"></script>
<script src="https://unpkg.com/react-dom@16.12.0/umd/react-dom.development.js"></script>
<script type="text/javascript">
  const rootElement = document.querySelector('#root');
  const element = React.createElement(
    'div', { 
    children: ['Hello World!', 'I am React'],
    className: 'container'
  });
  ReactDOM.render(element, rootElement);
</script>
```
