# React Concepts

## What is React?
React is an open source JavaScript Library for building user interfaces.  It is also known as React.js or ReactJS

**`React is a Component-based Library`**: create independent and useful UIs modules that can be reused.  All the functionality and state is encapsulated inside the component.  Conceptually, components are like JavaScript functions.  They accept arbitrary inputs (called "props") and return React elements describing what should appear on the screen.  

**`React is Declarative`**: describe how te app should look like and the framework will figure out how it will happen.  There is no need to explain step by step how the component will work, react will update base on the change of the state

## Model Data

### Props
Short for properties, props can be seen as the arguments that we passed in a function, in React props are objects and they are just a communication channel between components, always moving from top to bottom.

**`React is flexible but it has a single strict rule: React components must act like pure functions with respect to their props (Pure functions do not attempt to change their inputs, and always return the same result for the same inputs) `**

### State
It's a serializable representation of one point in time of the component, in other words, It's the status (value) of the component in a particular set time.  The component manages his own state internally and allows React components to change their output over time in response to user actions, network reponses and anything else.

## The Lifecycle
Each component has several "lifecycle method" that can be override to run code at particular times in the process, this will allow to perform certain actions when a component is created or destroyed or how must react to props or state changes.  By default, the only required method ever in a React component is render() {}, render() is responsible for returning the markup we'll actually show on screen.   Methods prefixed with **`will`** are called right before something happens, and methods prefixed with **`did`** are called right after something happend

### Initialization
The initialization phase is where we define defaults and initial values for this.props and this.state by implementing getDefaultProps() and getInitialState() respectively.

- `getDefaultProps()`: used to define any default props which can be accessed via this.props
- `getInitialState()`: enables to set the initial state value, that is accesible inside the component via this.state

### Mounting
Mounting is the process that occurs when a component is being inserted into the DOM. This phase has two methods that we can hook up with: componentWillMount() and componentDidMount()

- `componentWillMount()`: It’s invoked once and immediately before the initial rendering occurs, hence before React inserts the component into the DOM
- `componentDidMount():` is called just once and immediately after React inserts the component into the DOM. Now the updated DOM is available for access, which means that this method is the best place for initializing other Javascript libraries that need access to the DOM and for data fetching operations

### Updating
There are also methods that will allow us to execute code relative to when a component’s state or properties get updated. These methods are part of the updating phase and are called in the following order:

- `componentWillReceiveProps()`, invoked when a component is receiving new props. We can use this method as an opportunity to react to a prop transition before the render() method is called
- `shouldComponentUpdate()` method allows us to decide whether the next component’s state should trigger a re-render or not. This method returns a boolean value, which by default is true
- `componentWillUpdate()` method is called immediately before rendering, when new props or state are being received. We can use this as an opportunity to perform preparation before an updates occurs
- `componentDidUpdate()` method is called immediately after React updates the DOM. We can use this method to interact with the updated DOM or perform any action post-render

### Unmounting
In this phase React provide us with only one method: `componentWillUnmount()`

It is called immediately before the component is unmounted from the DOM. We can use it to perform any cleanup we might need, such as invalidating timers or cleaning up any DOM elements that were created in componentDidMount() / componentDidUpdate()

## Link
React Documentation: [`https://facebook.github.io/react/`](https://facebook.github.io/react/)






