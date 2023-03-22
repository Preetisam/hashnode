---
title: "What is a virtual DOM and Why is it used in libraries/frameworks?"
seoTitle: "How Virtual DOM Works"
seoDescription: "The Virtual DOM works by creating an in-memory representation of the actual DOM. Whenever a change is made to the user interface, the Virtual DOM is updated"
datePublished: Wed Feb 22 2023 06:45:38 GMT+0000 (Coordinated Universal Time)
cuid: clefba41006plhynv9mhs8lmd
slug: what-is-a-virtual-dom-and-why-is-it-used-in-librariesframeworks
cover: https://cdn.hashnode.com/res/hashnode/image/stock/unsplash/_t-l5FFH8VA/upload/2b5fd00339218080fceec41ae4ec4767.jpeg
tags: virtual-dom, framework, dom, libraries, benfits-of-using-virtual-dom

---

## **Table of Contents**

* Definition of Virtual DOM
    
* How Virtual DOM Works
    
* Virtual DOM in Libraries/Frameworks
    
* Benefits of Using a Virtual DOM
    

## **Definition of Virtual DOM**

A Virtual DOM (VDOM) is a programming concept used in libraries and frameworks for building user interfaces. It is an abstraction of the real DOM, which is the HTML Document Object Model that web browsers use to represent web pages.

## **How Virtual DOM Works**

The Virtual DOM works by creating an in-memory representation of the actual DOM. Whenever a change is made to the user interface, the Virtual DOM is updated, and the library compares the previous state of the Virtual DOM with the new state to determine what changes need to be made to the actual DOM. This approach is often more efficient than directly updating the DOM, as changes to the DOM can be expensive in terms of processing power and memory.

## **Virtual DOM in Libraries/Frameworks**

Libraries and frameworks such as React and Vue.js use a Virtual DOM to update the user interface efficiently. When an application built with one of these frameworks is loaded, the framework creates a Virtual DOM tree that reflects the initial state of the application's user interface. When a user interacts with the application and changes the state of the user interface, the framework updates the Virtual DOM tree to reflect these changes. The framework then calculates the minimal set of changes needed to update the actual DOM and performs those changes.

## **Benefits of Using a Virtual DOM**

Using a Virtual DOM provides a number of benefits for developers. It makes it easier to manage the complexity of user interfaces, as developers can work with a simple tree structure instead of directly manipulating the actual DOM. It also makes it easier to write code that is optimized for performance, as changes to the user interface can be batched and applied more efficiently.

The library/framework uses the virtual DOM as a means to improve performance. When the state of an application changes, the real DOM needs to be updated to reflect it. However, changing real DOM nodes is costly compared to recalculating the virtual DOM. The previous virtual DOM can be compared to the new virtual DOM very quickly in comparison.

Once the changes between the old VDOM and new VDOM have been calculated by the diffing engine of the framework, the real DOM can be patched efficiently in the least time possible to match the new state of the application.

Overall, the Virtual DOM is a powerful concept that has revolutionized the way that developers build user interfaces for the web. It provides a more efficient and intuitive way to work with the DOM, and has made it possible to create complex, dynamic user interfaces that are both responsive and fast.

### **I hope this glimpse into the inner workings of** Virtual DOM **and browsers has been helpful and illuminating. Thanks for coming along for the journey!**