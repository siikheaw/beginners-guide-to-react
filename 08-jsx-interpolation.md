# Understand and Use Interpolation in JSX

Consider this example:
```js
// The text "Hello World" has 11 characters
// The text "" has No characters

function CharacterCount({text}) {
  return (
    <div>
      // The text "text" has text.length characters
      {`The text "${text}" has `} <strong>{text.length}</strong> characters.
    </div>
  );
}

const element = (
  <>
    <CharacterCount text="Hello World" />
    <CharacterCount text="" />
  </>
);

ReactDOM.render(element, document.querySelector('#root');
```

This will compiled to:
```
The text "Hello World" has 11 characters
The text "" has 0 characters
```

For `""` What if we want to return 'No' instead of 0:
```js
function CharacterCount({text}) {
  const length = text.length ? text.length : 'No';
  return (
    <div>
      {`The text "${text}" has `} <strong>{length}</strong> characters.
    </div>
  );
}
```

or:
```js
function CharacterCount({text}) {
  const length = text.length ? text.length : 'No';
  return (
    <div>
      {`The text "${text}" as '}
      {text.length ? <strong>{text.length}</strong> : 'No'}
      {' characters'}
    </div>
  );
}
```

Having a good understand how Babel compiling JSX to JS will help using JSX more effectively.

