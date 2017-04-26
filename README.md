# React Concepts

## What is React?
React is an open source JavaScript Library for building user interfaces.  It is also known as React.js or ReactJS

**`React is a Component-based Library`**: create independent and useful UIs modules that can be reused.  All the functionality and state is encapsulated inside the component  Conceptually, components are like JavaScript functions.  They accept arbitrary inputs (called "props") and return React elements describing what should appear on the screen.  

**`React is Declarative`**: describe how te app should look like and the framework will figure out how it will happen.  There is no need to explain step by step how the component will work, react will update base on the change of the state

## Model Data

### Props
Short for properties, props can be seen as the arguments that we passed in a function, in React props are objects 

**`React is flexible but it has a single strict rule: React components must act like pure functions with respect to their props (Pure functions do not attempt to change their inputs, and always return the same result for the same inputs) `**

### State
It's a serializable representation of one point in time of the component, in other words, It's the status (value) of the component in a particular set time.  The component manages his own state internally and allows React components to change their output over time in response to user actions, network reponses and anything else.

## The Lifecycle
Each component has several "lifecycle method" that can be override to run code at particular times in the process, this will allow to perform certain actions when a component is created or destroyed or how must react to props or state changes.  Methods prefixed with **`will`** are called right before something happens, and methods prefixed with **`did`** are called right after something happend

### Initialization
During this process, the following methods are called:

getInitialState
getDefaultProps
ComponentWillMount
Render
ComponenDidMount

This 2 methods are only called once when initially rendering the component
- getInitialState: enables to set the initial state value, that is accesible inside the component via this.state
- getDefaultProps: used to define any default props which can be accessed via this.props


This 2 methods are only called when initializing a component
- componentWillMount: is called before the render method is executed
- componentDidMount: is called as soon as the render method has been executed

## Link
React Documentation: [`https://facebook.github.io/react/`](https://facebook.github.io/react/)