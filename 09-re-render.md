# Rerender a React Application

Updating the DOM is typically the slowest part of the whole process. React only updates what's necessary.

React DOM compares the element and its children to the previous one, and only applies the DOM updates necessary to bring the DOM to the desired state.

The normal JavaScript app:
```js
const rootElement = document.querySelector('#root');

function tick() {
  const time = new Date().toLocaleTimeString();
  const element = `
    <div>Hello</div>
    <div>${time}</div>;
    <input value="${time}" />
  `

  rootElement.innerHTML = element;
}

tick();
setInterval(tick, 1000);
```

With this app, the entire app (`tick()`) will be updated every second.

The React app:
```js
const rootElement = document.querySelector('#root');

function tick() {
  const time = new Date().toLocaleTimeString();
  const element = 
    <div>Hello</div>
    <div>{time}</div>;
    <input value={time} />

  ReactDOM.render(element, rootElement);
}

tick();
setInterval(tick, 1000);
```

Even though we create an element describing the whole UI tree on every tick, only the text node whose contents have changed gets updated by React DOM.
