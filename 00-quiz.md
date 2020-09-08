# Quiz

## 3. Convert this to the JavaScript (React.createElement) equivalent:
```js
<div id='greeting' className='active'>Hello {user.name}</div>
```

Answer:
```js
const element = React.createElement('div', 
  {
    id: 'greeting',
    className: 'active'
  },
  'Hello ',
  user.name
);
```

### 11. How do you add interactivity when a component is clicked?
Answer:
Add an `onClick` prop, and pass it a function. The function will be called every time the component is clicked.
```js
<button onClick={() => console.log('clicked!');}>Click me</button>
```
