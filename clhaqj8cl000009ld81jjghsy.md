---
title: "Embedding and Referencing"
seoTitle: "Embedding and Referencing"
seoDescription: "Embedding means you can store the subdocuments directly within the main document. This is useful when the embedded data"
datePublished: Fri May 05 2023 15:52:54 GMT+0000 (Coordinated Universal Time)
cuid: clhaqj8cl000009ld81jjghsy
slug: embedding-and-referencing
cover: https://cdn.hashnode.com/res/hashnode/image/stock/unsplash/3BgkveM3y_k/upload/80181664e2640ae3d3ce69ee1bb35bd8.jpeg
tags: mongodb, referencing, embedding

---

In MongoDB, you can store related data either by embedding or referencing it.

Embedding means you can store the subdocuments directly within the main document. This is useful when the embedded data is relatively small and not frequently accessed. This approach removes the need for additional queries and reduces the complexity of the data model. Here's how you can embed related data in a MongoDB document using the example of a blog post and its comments in JavaScript:

```javascript
{
   _id: ObjectId("60a63213bd2b0f197c3f3d1d"),
   title: "My First Blog Post",
   content: "This is my first blog post on Hashnode.",
   comments: [
      { author: "user1", text: "Great post." },
      { author: "user2", text: "Thanks for sharing." }
   ]
}
```

Referencing, on the other hand, means storing a reference to a related document rather than embedding the entire document. This is useful when the related data is complex or frequently accessed, as it allows for greater flexibility in querying and updating the data. Here's an example of referencing related data in MongoDB using the same blog post and comment entities as above:

```javascript
// Blog Post Document
{
   _id: ObjectId("60a63213bd2b0f197c3f3d1d"),
   title: "My First Blog Post",
   content: "This is my first blog post on Hashnode.",
   comments: [
      ObjectId("60a63213bd2b0f197c3f3d1e"),
      ObjectId("60a63213bd2b0f197c3f3d1f")
   ]
}

// Comment Document
{
   _id: ObjectId("60a63213bd2b0f197c3f3d1e"),
   author: "user1",
   text: "Great post."
}

{
   _id: ObjectId("60a63213bd2b0f197c3f3d1f"),
   author: "user2",
   text: "Thanks for sharing."
}
```

In this example, the blog post document includes an array of comment IDs, which can be used to retrieve the corresponding comment documents using a separate MongoDB query.