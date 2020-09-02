# JSX

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
