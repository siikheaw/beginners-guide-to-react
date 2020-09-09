# Use JSX effectively with React

JSX is not an entirely different language, but it is a bit of an extension to the language, so knowing how you would express certain JavaScript things withing the JSX syntax is important to using JSX effectively.

To interpolation use `{}`. Any JavaScript expression inside of the curly braces will be evaluated and passed to the `React.createElement` API. This allows you tu be expressive when building out Ui's.

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
The spread operator takes either an array or an object and expands it into its set of items. We can use the spread operator to pass down our props to the `React.createElement` API:
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
