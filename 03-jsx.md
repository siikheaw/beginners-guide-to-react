# JSX

JSX is a JavaScript extension which is HTML like syntax. To use JSX in a browser, we must use Babel to compile JSX to normal JavaScript.

```html
<div id="root"></div>
<!-- Get React from UNPKG -->
<script src="https://unpkg.com/react@16.12.0/umd/react.development.js"></script>
<script src="https://unpkg.com/react-dom@16.12.0/umd/react-dom.development.js"></script>
<!-- Load Babel -->
<!-- v6 <script src="https://unpkg.com/babel-standalone@6/babel.min.js"></script> -->
<script src="https://unpkg.com/@babel/standalone/babel.min.js"></script>

<script type="text/babel">
  const rootElement = document.querySelector('#root');
  /*
  const element = React.createElement(
    'div', { 
    children: ['Hello World!', 'I am React!'],
    className: 'container'
  });*/
  
  /* JSX */
  const element = <div className="container">Hello World! I am React!</div>;
  
  ReactDOM.render(element, rootElement);
</script>
```

### Recap
- To use JSX in a browser, must include Babel to compile JSX to JavaScript.
- Change `<script type="text/javascript">` to `<script type="text/babel">`
