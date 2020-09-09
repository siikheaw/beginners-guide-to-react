# Create a User Interface with Vanilla Javascript and DOM

- To create a user interface with JavaScript you will need a place to append your JavaScript DOM elements. This will be the `root` of our application.
- Get access to that element using the document's API.
- We create our element and add properties to it.
- Finally, appended it to the DOM element.

```html
<div id="root"></div> <!-- The App will be mounted here -->
<script type="text/javascript">
  const rootElement = document.querySelector('#root');// Select the root element
  const element = document.createElement('div');      // Create an element with `document.createElement`
  element.textContent = 'Hello World!';               // Set text inside `element`
  element.className = 'container';                    // Set `container` class to `element`
  rootElement.appendChild(element);                   // Append `element` to the `rootElement`
</script>
```
