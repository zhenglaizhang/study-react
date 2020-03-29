# Modern Javascript (ES2015+)

- arrow functions
- destructuring
- rest/spread operators
- classes

## Why React

- A JavaScript library for building user interfaces
- Not framework, small, not a completed solution
- Declarative for dynamic data
- model UI and state
- https://jscomplete.com/learn/why-react

## Hello

- https://jscomplete.com/playground
- Chrome React Developer Tools extension
- https://reactjs.org/docs/introducing-jsx.html
- https://facebook.github.io/jsx/
- https://babeljs.io/rep

```
function Hello() {
	// return <div>Hello React!</div>;
  return React.createElement("div", null, "Hello React!")
}

ReactDOM.render(
  <Hello />, //  React.createElement(Hello, null),
  document.getElementById('mountNode'),
);
```

### useState

```
function Button() {
  const [counter, setCounter] = useState(1);
	return <button onClick={ () => setCounter(counter+1) }>{counter}</button>;
}

ReactDOM.render(
  <Button />, 
  document.getElementById('mountNode'),
);
```

### Parent -> Children data flow

```jsx
function Button(props) {
  return (
    <button onClick={ props.handleClick }>
      +1
    </button>
  )
}

function Display(props) {
  return <div>{props.couter}</div>;
}

function App() {
  const [counter, setCounter] = useState(1);
  const handleClick = () => setCounter(counter+1);
  return <React.Fragment>
    <Button handleClick={handleClick}/>
    <Display couter={counter} />
    </React.Fragment>; 
}

ReactDOM.render(
  <App />,
  document.getElementById('mountNode'),
);
```
### Smart diffing algorithm

- regenerate dom node if necessary only
- rethink how to update UI interface - let react figure out what should be updated in an efficient way


### Modern Javascript

- https://github.com/tc39
- https://jscomplete.com/learn
  - https://jscomplete.com/learn/complete-intro-modern-javascript/1mjs5-destructuring

## Resources

- https://reactjs.org/
- https://react-bootstrap.github.io/components/spinners/
- https://jscomplete.com/learn/react-beyond-basics/react-cfp