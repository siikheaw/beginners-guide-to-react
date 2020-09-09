# Create a User Interface with React’s JSX syntax

React team came up with **JSX**. It's an extension to the JavaScript language to support syntax that looks similar to the HTML that you would write to crete these DOM elements.

JSX gives us an expressive syntax for representing our UI, without losing the benefits and powers of writing our UI in the JavaScript.

The best way to take advantage of this is to learn how JSX is compiled to regular JavaScript by using Babel.

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
- Spend some time exploring how Babel compiles JSX, this will help you be more effective when using JSX.
