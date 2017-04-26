# React Concepts

## What is React?
React is an open source JavaScript Library for building user interfaces.  It is also known as React.js or ReactJS

**`React is a Component-based Library`**: create independent and useful UIs modules that can be reused.  All the functionality and state is encapsulated inside the component  Conceptually, components are like JavaScript functions.  They accept arbitraryinputs (called "props") and return React elements describing what should appear on the screen.  

**`React is Declarative`**: describe how te app should look like and the the framework will figure out how it will happen.  There is no need to explain step by step how the component will work, react will update base on the change of the state

## Model Data

### Props

### State

## The Lifecycle
Each component has several "lifecycle method" that can be override to run code at particular times in the process.  Methods prefixed **`will`** are called right before something happens, and methods prefixed with **`did`** are called right after something happend

### Initialization

This 2 methods are only called once when initially rendering the component
getInitialState: enables to set the initial state value, that is accesible inside the component via this.state
getDefaultProps: used to define any default props which can be accessed via this.props


This 2 methods are only called when initializing a component
componentWillMount: is called before the render method is executed
componentDidMount: is called as soon as the render method has been executed

## Link
React Documentation: [`https://facebook.github.io/react/`](https://facebook.github.io/react/)