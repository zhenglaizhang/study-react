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

## Resources

- https://reactjs.org/
- https://react-bootstrap.github.io/components/spinners/
- https://jscomplete.com/learn/react-beyond-basics/react-cfp