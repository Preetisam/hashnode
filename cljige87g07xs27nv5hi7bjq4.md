---
title: "Native Bridge"
seoTitle: "Native Bridge"
seoDescription: "Native bridge or the Native Module API is a way of communicating between native code and JavaScript code in React Native. It provides a way for React Native"
datePublished: Fri Jun 30 2023 10:50:39 GMT+0000 (Coordinated Universal Time)
cuid: cljige87g07xs27nv5hi7bjq4
slug: native-bridge
tags: native-module-api, native-bridge, native-functions, optimize-performance, prevent-overloading

---

Native bridge or the Native Module API is a way of communicating between native code and JavaScript code in React Native. It provides a way for React Native apps to access platform-specific features and APIs that are not available in JavaScript.

In React Native, the app code is written in JavaScript and executed through a JavaScript virtual machine. However, many platform-specific features such as accessing the device's camera or making a native call to the phone's dialer are not available in JavaScript.

To solve this problem, the Native Module API provides a way for React Native apps to bridge the gap between JavaScript and native code. It allows the app to call a native module, which is a set of native functions, from the JavaScript code.

To create a native module, you need to write both the JavaScript and native code. In JavaScript, you define the interface for the native module and call the native function using the `NativeModules` module. In native code, you implement the native functions.

Here's an example of creating a native module:

**JavaScript**

```javascript
import { NativeModules } from 'react-native';

const { MyNativeModule } = NativeModules;

MyNativeModule.doSomething();
```

**Native Code**

```java
package com.myapp.mynativemodule;

import com.facebook.react.bridge.ReactApplicationContext;
import com.facebook.react.bridge.ReactContextBaseJavaModule;
import com.facebook.react.bridge.ReactMethod;

public class MyNativeModule extends ReactContextBaseJavaModule {

  public MyNativeModule(ReactApplicationContext reactContext) {
    super(reactContext);
  }

  @Override
  public String getName() {
    return "MyNativeModule";
  }

  @ReactMethod
  public void doSomething() {
    // implementation of the native function
  }
}
```

In the above example, `MyNativeModule` is a custom native module that can be called from JavaScript using the `NativeModules` module. The `doSomething()` the function is the native code that is executed when the `MyNativeModule.doSomething()` the method is called JavaScript.

The Native Bridge is responsible for transporting data between these two threads, and this can be a resource-intensive task. When the Native Bridge receives a lot of data, it can slow down the app and negatively impact the user experience, especially if there are animations involved.

How to optimize performance and prevent overloading of the Native Bridge?

To optimize performance and prevent overloading of the Native Bridge, it's important to follow some best practices:

1. Avoid sending large amounts of data over the bridge in a single go, if possible.
    
2. Minimize the usage of the bridge as much as possible by utilizing pure JavaScript as much as possible.
    
3. Optimize animations to avoid too much data being sent between the bridge.
    
4. Use libraries that have been optimized for performance to help minimize the impact on the Native Bridge.
    

By following these best practices, you can help prevent overloading the Native Bridge and ensure that your app runs smoothly and performs as expected.

**Summary:**

Native Bridge and how it impacts the performance of a mobile application. Native Bridge is a communication layer that allows React Native to communicate with native modules. The Native Bridge is used to send data between the JavaScript and native threads. In simple terms, if an app has a React Native component and a native module working together, they would be communicating with each other using the Native Bridge.