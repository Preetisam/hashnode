---
title: "React Router Params"
seoDescription: "URL parameters and query parameters can be used to customize the behavior of a component based on the current URL. For example, you could use URL parameters"
datePublished: Fri Mar 24 2023 17:36:22 GMT+0000 (Coordinated Universal Time)
cuid: clfmtqi8l000009lahyoy3479
slug: react-router-params
cover: https://cdn.hashnode.com/res/hashnode/image/stock/unsplash/zNRITe8NPqY/upload/679d92c26bd44af50e93ca73d2d6d7d2.jpeg
tags: reactjs, components, reacthooks, react-router-6

---

In React, "params" usually refer to URL parameters or query parameters that are passed to a component via its props.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1679676740630/bdf043b7-2640-42ce-a604-ae08d225e62a.png align="center")

```javascript
import React from 'react'
import { useParams } from 'react-router-dom'

//This the user component page where we are using useParms hook from the react routerdom 
const User = () => {
// declaring  the params to useParms
    const params =useParams();
//we are using name as params to declare mutiple users instead of single user
    const {name}=params
    //console.log(name)
  return (
    <div>
      <h1>This is {name} page</h1>
    </div>
  )
}

export default User
```

```javascript
import React from 'react'
import {Link} from 'react-router-dom' 
const About = () => {
  return (
    <div>
    <h1>AboutPage</h1>
  
    <li><Link to="/user/preeti">Preeti</Link></li>
    <li><Link to="/user/elena">Elena grace</Link></li>

    </div>
  )
}

export default About
```

```javascript

import React from 'react'
import "./App.css"
import Home from './Component/Home'
import Nav from './Component/Nav'
import About from './Component/About'
import Services from './Component/Services'
import ContactUs from './Component/ContactUs'
import ErrorPage from './Component/ErrorPage'
import {BrowserRouter as Router, Routes, Route, Navigate} from 'react-router-dom'

import User from './Component/User'
const App = () => {
  return (
    <div>
<Router>
    <Nav/>
    <Routes>
        <Route path="/" element={<Home/>}/>
        <Route path="/about" element={<About/>}/>
        <Route path="/services" element={<Services/>}/>
        <Route path="/contactus" element={<ContactUs/>}/>
        <Route path="/*" element={<ErrorPage/>}/>
        <Route path="/*" element={<Navigate to ="/"/>}/>
        <Route path="/user/:name" element={<User/>}/>
    </Routes>
</Router>
    </div>
  )
}

export default App
```

URL parameters are part of the URL path and are used to identify a specific resource. For example, in the URL [http://localhost:3000/user/preeti](http://localhost:3000/user/preeti), "Preeti" is a URL parameter that identifies the user with the name Preeti. In React, you can access URL parameters using the `useParams` hook, which returns an object containing the parameter values. we are passing the

In App.js file we are in router **&lt;Route path="/user/:name" element={&lt;User/&gt;}/&gt;** we can use **name** parameters for multiple users.

Here in User.js component, we are **import { useParams } from 'react-router-dom**' in the users component declaring params

**const params =useParams();**

Query parameters are optional key-value pairs that can be added to a URL to provide additional information about the request. For example, in the URL [`https://example.com/search?q=react`](https://example.com/search?q=react), "q" is a query parameter with the value "react". In React, you can access query parameters using the `useLocation` hook to get the current URL and then parse the query string using the `query-string` library or a similar tool.

Both URL parameters and query parameters can be used to customize the behavior of a component based on the current URL. For example, you could use URL parameters to show a specific user's profile or use query parameters to filter search results.