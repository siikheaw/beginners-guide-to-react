# Use Event Handlers with React

Let's get an introduction to event handlers with React. There are a ton of supported events that you can find on the docs. 

We still haven't gotten to state yet, so we've implemented our own little way of managing state and re-rendering our component so we can play around with event handlers.

One thing you'll want to know is that events with React are very similar to working with events in regular DOM.

```js
const rootElement = document.querySelector('#root');

const state = {eventCount: 0, username: ''};

function App() {
  function handleClick() {
    setState({eventCoung: state.eventCount + 1});
  }
  
  function handleChange() {
    setState({username: event.target.value});
  }
  
  return (
    <div>
      <p>There have been {state.eventCount} events.</p>
      <p><button onClick={handleClick}>Click me</button></p>
      <p>You typed: {state.username}</p>
      <p><input onBlur={handleChange} /></p>
    </div>
  );
}

function setState(newState) {
  Object.assign(state, newState);
  renderApp();
}

function renderApp() {
  ReactDOM.render(<App />, rootElement);
}

renderApp();
```

React does have an optimization implementation on top of the event system called SyntheticEvents, but most of the time you won't observe any difference with those events from regular DOM events (and you can always get access to the native event using the nativeEvent property).
