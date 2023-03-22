---
title: "Two ways to Manage State in React - useState and setState"
seoTitle: "React Hooks State Management  setState method  useState hook"
seoDescription: "React is a popular JavaScript library for building user interfaces. It allows developers to create reusable components that can be easily composed to create"
datePublished: Thu Jan 19 2023 19:37:42 GMT+0000 (Coordinated Universal Time)
cuid: cld3hw12o000109mg6j4yhb4v
slug: two-ways-to-manage-state-in-react-usestate-and-setstate
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1674155853262/bf9113b1-0970-4f85-8943-e8e371eafe67.png
tags: web-development, react-usestate-state-management-hooks-components-javascript-front-end-development-web-development-code-examples-step-by-step-guide-user-interfaces-programming-tutorial-web-development-tutorial-javascript-development-react-development-reactjs-state-hook-state-management-in-react-frontend-development

---

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1674155812228/287045ea-ac73-466e-883c-cb67bfe0d04f.png align="center")

**Introduction to state management in React**

React is a popular JavaScript library for building user interfaces. It allows developers to create reusable components that can be easily composed to create complex user interfaces. One of the key features of React is its ability to manage and update the state of a component. In this article, we will take a look at two ways to manage the state in React: the useState hook and the setState method.

**Managing state with the useState hook**

The useState hook is a new way to manage state in functional components introduced in React 16.8. It allows you to add a state to a functional component without the need for a class component. The useState hook takes a single argument, which is the initial state and returns an array with two elements: the current state and a function to update the state. Here's an example of how to use the useState hook:

**Syntax and usage:** In the above example, we are using the useState hook to add a state variable called "count" to our component. The initial value of the count is set to 0. We are also using a button that, when clicked, calls the setCount function to increment the count by 1.

**Managing state with the setState method**

The setState method is the traditional way to manage the state in React class components. It allows you to update the state of a component and re-render the component with the updated state. The setState method takes an object or a function that updates the state, and React will automatically re-render the component with the updated state. Here's an example of how to use the setState method:

**Syntax and usage:** For example above image, we are using the setState method to update the "count" state variable when the button is clicked. The handle inclement function is called when the button is clicked, and it uses the setState method to update the count by 1. React will then re-render the component with the updated count.

1. **Comparing useState and setState:** Pros and consBoth useState and setState method have their own advantages, useState is more simple and less verbose, and it's suitable for most cases.
    
2. **Best practices for state management in React:** However, setState is more powerful and allows you to handle more complex cases. It's important to note that setState is going to be deprecated and will not be available in the next versions of React.
    
    **Conclusion: Choosing the right state management method for your use case.**
    
    In conclusion, React's useState hook and setState method are two ways to manage state in React. The useState hook is a new way to manage state in functional components, while the setState method is the traditional way to manage state in class components. Both have their own advantages, and it's important to choose the right one depending on your use case.