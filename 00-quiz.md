# Quiz

## 3. Convert this to the JavaScript (React.createElement) equivalent:
```jsx
<div id='greeting' className='active'>Hello {user.name}</div>
```

Answer:
```jsx
const element = React.createElement('div', 
  {
    id: 'greeting',
    className: 'active'
  },
  'Hello ',
  user.name
);
```
