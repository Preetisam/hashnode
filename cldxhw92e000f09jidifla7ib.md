---
title: "What is REST?"
seoDescription: "REST stands for Representational State Transfer and is a software architectural style for creating web services. REST is based on the HTTP protocol"
datePublished: Thu Feb 09 2023 19:30:58 GMT+0000 (Coordinated Universal Time)
cuid: cldxhw92e000f09jidifla7ib
slug: what-is-rest
cover: https://cdn.hashnode.com/res/hashnode/image/stock/unsplash/2JIvboGLeho/upload/53d47b9b8478c334315080c5ab85ab36.jpeg
tags: https, apis, reactjs, crud

---

REST stands for **Representational State Transfer** and is a software architectural style for creating web services. REST is based on the HTTP protocol and is used for building web APIs (Application Programming Interfaces) that allow communication between different systems over the internet. A RESTful web application exposes data in the form of information about its resources.

RESTful web services are stateless, meaning that they do not store client data on the server between requests. Instead, all data is sent as part of the request and response. This enables RESTful web services to be scalable and flexible.

A RESTful API uses a set of standard HTTP methods. Generally, this concept is used in web applications to manage state. With most applications, there is a common theme of reading, creating, updating, and destroying data.

Data is modularized into separate tables like `posts`, `users`, `comments`, and a RESTful API exposes access to this data: to perform operations on resources identified by URIs (Uniform Resource Identifiers). The resources are typically represented as JSON or XML data, and the API defines how to interact with them.

REST is widely adopted due to its simplicity, scalability, and compatibility with a variety of programming languages and platforms. It is used to build a variety of applications, including web-based, mobile, and cloud-based applications.

Generally, this concept is used in web applications to manage state. With most applications, there is a common theme of reading, creating, updating, and destroying data. Data is modularized into separate tables like `posts`, `users`, `comments`, and a RESTful API exposes access to this data with:

* **An identifier for the resource. This is known as the endpoint or URL for the resource.**
    
* **The operation the server should perform on that resource in the form of an HTTP method or verb. The common HTTP methods are GET, POST, PUT, and DELETE.**
    

Here is an example of the URL and HTTP method with a `posts` resource:

* **Reading:** `/posts/` =&gt; GET
    
* **Creating:** `/posts/new` =&gt; POST
    
* **Updating:** `/posts/:id` =&gt; PUT
    
* **Destroying:** `/posts/:id` =&gt; DELETE