# Use JSX effectively with React

Anything in `{}` can be a JavaScript expressions.
```jsx
const myChildren = 'Hello World!';
const myClassName = 'container';
const element = <div className={className}>{children}</div>;
```

Will be compiled to:
```jsx
var element = React.createElement('div', {className: myClassName}, myChildren);
```

Babel will leave anything in `{}` alone, and pass it directly as the properties.


```jsx
const element = (
  <div className={className}>
    <span>Hello</span> <strong>World!</strong>
  </div>
);
```

Will be compiled to:
```jsx
var element = 
  React.createElement('div', {className: className},
  React.createElement('span', null, 'Hello'), 
  ' ',
  React.createElement('strong', null, 'World!')
);
```

`children` is also a props, so we can put it at the props position:
```jsx
const element = <div className={className}>{children}</div>
// `children` is a props too
const element = <div className={className} children={children}></div>
```
                
## Using Spread Operator with Props
```jsx
const props = {children, className};
const element = <div {...props}></div>
```

Will be compiled to:
```jsx
var props = {
  children: children,
  className: className
};
var element = React.createElement('div', props);
```
