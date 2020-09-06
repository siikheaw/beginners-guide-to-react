# Rerender a React Application

When render the application, React will only update the parts that actually changed.

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

With React app, only parts that need to be update will be re-rendered.
