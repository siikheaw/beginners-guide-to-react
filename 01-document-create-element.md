# Create a User Interface with Vanilla Javascript and DOM

```html
<div id="root"></div> <!-- The App will be mounted here -->
<script type="text/javascript">
  const rootElement = document.querySelector('#root');// Select the root element
  const element = document.createElement('div');      // Create an element
  element.textContent = 'Hello World!';               // Set text inside `element`
  element.className = 'container';                    // Set `container` class to `element`
  rootElement.appendChild(element);                   // Append `element` to the `rootElement`
</script>
```
