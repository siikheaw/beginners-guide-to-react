# Create a User Interface with React's createElement API
To use React, we need to install **npm**, or using [unpkg](https://unpkg.com/).

```html
<div id="root"></div>
<!-- Get React from UNPKG -->
<script src="https://unpkg.com/react@16.12.0/umd/react.development.js"></script>
<script src="https://unpkg.com/react-dom@16.12.0/umd/react-dom.development.js"></script>
```

We can create element using React's createElement API:
```js
const element = React.createElement('div' {
  children: 'Hello World!',
  className: 'container'
});
```

Full code: https://codesandbox.io/s/upbeat-greider-eq2wy?fontsize=13&hidenavigation=1&theme=dark
```html
<div id="root"></div>
<!-- Get React from UNPKG -->
<script src="https://unpkg.com/react@16.12.0/umd/react.development.js"></script>
<script src="https://unpkg.com/react-dom@16.12.0/umd/react-dom.development.js"></script>
<script type="text/javascript">
  const rootElement = document.querySelector('#root');
  const element = React.createElement(
    'div', {                                    // element 
    children: ['Hello World!', 'I am React'],   // props.children
    className: 'container'                      // props.className
  });
  ReactDOM.render(element, rootElement);
</script>
```
