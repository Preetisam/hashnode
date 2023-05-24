---
title: "setState Call Back"
seoTitle: "setState Call Back"
seoDescription: "React state updates may sometimes be asynchronous which means that if you access the state value immediately after calling, it may not have updated yet."
datePublished: Wed May 24 2023 13:34:28 GMT+0000 (Coordinated Universal Time)
cuid: cli1qydn5000r0al9arlw9zny
slug: setstate-call-back
tags: components, set-state-call-back, re-rendered

---

In React state updates may sometimes be asynchronous which means that if you access the state value immediately after calling, it may not have updated yet. To handle situations like this, `setState()` a method in React can take a callback function as its second argument. This callback function will execute only after the state has been updated, which means you will have access to the updated state value inside the callback function.

Here's an example of a `setState()` call with a callback function:

```jsx
class MyComponent extends React.Component {
  constructor(props) {
    super(props);
    this.state = {
      counter: 0
    };
  }

  handleClick = () => {
    this.setState(prevState => ({
      counter: prevState.counter + 1
    }), () => {
      console.log('State updated:', this.state.counter);
    });
  }

  render() {
    return (
      <div>
        <p>Counter: {this.state.counter}</p>
        <button onClick={this.handleClick}>Increment</button>
      </div>
    );
  }
}
```

In the example above, `setState()` method is called with an updater function that takes in the previous state value and returns the new state value. The second argument is a callback function that prints the updated state value to the console after it has been updated. This ensures that the updated state value is available inside the callback function.

Using the callback function in this way can help you manage scenarios where you need to update state and then perform some action after the update is complete.

the second argument to `setState()` method is a callback function, which is executed after the state has been updated. This callback function receives the updated state as an argument, so you can access it and perform any necessary operations.

Regarding binding the callback function, it's a good practice to bind it in the constructor method to avoid creating a new function every time the component is re-rendered. This can cause unnecessary re-renders and affect the performance of the application.

Here's an example of how to bind the callback function in the constructor method:

```javascript
class MyComponent extends React.Component {
  constructor(props) {
    super(props);
    this.state = {
      counter: 0
    };
    this.handleStateUpdate = this.handleStateUpdate.bind(this);
  }

  handleClick = () => {
    this.setState(prevState => ({
      counter: prevState.counter + 1
    }), this.handleStateUpdate);
  }

  handleStateUpdate(updatedState) {
    console.log('State updated:', updatedState.counter);
  }

  render() {
    return (
      <div>
        <p>Counter: {this.state.counter}</p>
        <button onClick={this.handleClick}>Increment</button>
      </div>
    );
  }
}
```

In the example above, `handleStateUpdate()` the function is bound to the component instance in the constructor method, which ensures that the same function instance is used every time the component is re-rendered. The function receives the updated state as an argument, which can be used to perform any necessary operations. The bound function is then passed as the second argument to `setState()` method.