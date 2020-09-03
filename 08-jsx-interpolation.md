# Understand and Use Interpolation in JSX

```js
// The text "Hello World" has 11 characters
// The text "" has No characters

function CharacterCount({text}) {
  return (
    <div>
      // The text "text" has text.length characters
      {`The text '${text}' has `} {text.length} characters.
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

