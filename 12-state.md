# Manage state in a React Component with the useState hook

> An application that responds to user input is valuable, but what do we do with that data the user has given us? This is where component state comes in. We need a place to put data that can change in our application, and we need to let React know when that state changes so it can update (or re-render) our app for us.
>
> In React, state is associated to components and when the state changes, the component is updated. To get access to this state and to update it, we use what is called a “React Hook” which allows us to call into React from within our component and let it know that we need to manage some state. In this lesson, you’ll learn how to use the `useState` hook to do this.

An application that responds to user input is valuable, but what do we do with that data the user has given us? This is where the component state comes in.

We need a place to put data that change in our application, and we need to let React know when that state changes so it can update (or re-render) our app for us.

In React, the state is associated with components and when the state changes, the component is updated.

To get access to this state and to update it, we use what is called a **React Hook** which allows us to call into React from within our component and let it know that we need to manage some state.

```js
function Greeting() {
  // useState - Returns a stateful value, and a function to update it.
  // During the initial render, the returned state (state) is the same
  // as the value passed as the first argument (initialState).
  const [name, setName] = React.useState('');
  // The setState function is used to update the state.
  // It accepts a new state value and enqueues a re-render of the component.
  // During subsequent re-renders, the first value returned by useState
  // will always be the most recent state afte applying updates.
  
  const handleChange = event => setName(event.target.value);
  return (
    <div>
      <form>
        <label htmlFor="name>Name: </label>
        <input onChange={handleChange} id="name" />
      </form>
      {name ? <strong>Hello {name}</strong> : 'Plae type your name'}
    </div>
  );
}
```
