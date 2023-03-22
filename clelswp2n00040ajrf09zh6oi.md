---
title: "What is the Difference Between Component DidMount and Component DidUpdate"
seoTitle: "Difference Between Component DidMount and Component DidUpdate"
seoDescription: "componentDidMount() is called once when the component is first mounted, while componentDidUpdate() is called every time the component is updated.Read more.."
datePublished: Sun Feb 26 2023 19:45:43 GMT+0000 (Coordinated Universal Time)
cuid: clelswp2n00040ajrf09zh6oi
slug: what-is-the-difference-between-component-didmount-and-component-didupdate
tags: reactjs, frontend-development, componentdidmount, componentdidupdate

---

Welcome to my blog, In this blog post, we will explore the difference between DidMount and DidUpdate in React.

**componentDidMount()** and **componentDidUpdate()** are lifecycle methods in **React** that are called at different stages of a component's lifecycle.

**componentDidMount()** is called **once**, immediately after a component is mounted (i.e., inserted into the **DOM tree**). This method is typically used to perform **initialization tasks**, such as fetching data from an external source or setting up event listeners.

```javascript
import React from "react";
import "./App.css";

// Life cycle components Component Did Mount

class App extends React.Component() {
  constructor() {
    super();
    this.state = {
      name: "preeti",
    };
    // console.warn("constructor");
  }

  componentDidMount() {
    console.warn("componentDidount");
  }
  render() {
    console.warn("render");
    return (
      <div className="App">
        <h1>Component DidMount{this.state.name}</h1>
        <button
          onClick={() => {
            this.setState({ name: "kamilla" });
          }}
        >
          Update Name
        </button>
      </div>
    );
  }
}
export default App;
```

**componentDidUpdate()** is called **after a component's state or props** have been updated and the component has been **re-rendered**. This method is typically used to perform tasks that need to be updated in response to changes in the component's state or props, such as updating the DOM or fetching new data based on the new **state or props.**

```javascript
import React from "react";
import "./App.css";
//Lifecycle  componentDidUpdate
class App extends React.Component() {
  constructor() {
    super();
    console.warn("constructor");
    this.state = {
      // name: "preeti",
      count: 0,
    };
  }
  //this will update the pervious and persent state

  componentDidUpdate(perProps, perState, snapShot) {
    //sanpashot gives us undefined when it is executed
    console.warn("ComponentDidUpdate", perState.count, this.state.count);
    // if (perState.count === this.state.count) {
    //   alert("data is already same");
    // }
    //infinte loop and send us the max depth achived
    //this.setState({ count: this.state.count + 1 });
    //instead we can make a condition for this to stop going it into infinite loop
    if (this.state.count < 10) {
      this.setState({ count: this.state.count + 1 });
    }
  }
  render() {
    console.warn("render");

    return (
      <div className="App">
        <h1>Component Did Update{this.state.count}</h1>
        {/* <button
          onClick={() => {
            this.setState({ name: "Kamilla" });
          }}
        ></button> */}
        {/* <button
          onClick={() => {
            this.setState({ count: this.state.count + 1 });
          }}
        >
          Update Name
        </button> */}
        <button
          onClick={() => {
            this.setState({ count: 1 });
          }}
        >
          Update Name
        </button>
      </div>
    );
  }
}
export default App;

//can  we make conditions in render or update state in render method?
//no we should not update the state in the render method because it update automaically so when we want to update the state we should do it in the component
//can we stop the component did mount method?
// yes we can stop the component didmount method to stop shouldComponentUpdate() return false
```

In summary, **componentDidMount()** is called once when the component is first mounted, while **componentDidUpdate()** is called **every time the component is updated**. **componentDidMount()** is typically used for **initialization tasks**, while **componentDidUpdate()** is typically used for tasks that need to be updated in response to changes in the component's state or props.

Hope you understood the concepts follow for more such updates. I am open to suggestions and queries. Feel free to ping me. you can follow me on [Twitter](https://twitter.com/preeti_samuel1) and [Linkedin](https://www.linkedin.com/in/preeti-samuel-5a247962/).