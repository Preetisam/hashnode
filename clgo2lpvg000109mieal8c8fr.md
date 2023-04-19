---
title: "What is Regex"
seoTitle: "What is Regex"
seoDescription: "Regex (short for "regular expression") is a pattern used in programming to match and manipulate strings of text. It is a sequence of characters that define"
datePublished: Wed Apr 19 2023 19:12:04 GMT+0000 (Coordinated Universal Time)
cuid: clgo2lpvg000109mieal8c8fr
slug: what-is-regex
cover: https://cdn.hashnode.com/res/hashnode/image/stock/unsplash/cijiWIwsMB8/upload/25fcf759feab03c5945f854791ae5d35.jpeg
tags: mongodb, regex, regular-expressions

---

Regex (short for "regular expression") is a pattern used in programming to match and manipulate strings of text. It is a sequence of characters that define a search pattern. Regex is commonly used in programming languages and text editors to perform tasks such as data validation, data extraction, and search and replace operations.

Regex patterns are made up of a combination of alphanumeric characters and special characters that have specific meanings. For example, the character "." (period) in a regex pattern matches any single character, while the character "\*" (asterisk) matches zero or more occurrences of the preceding character or group. Regex can be very powerful and flexible, but also somewhat complex and difficult to understand for those not familiar with it.

how to find the Max in the database? //db.coll.find({name: /^Max/})

The MongoDB query `db.coll.find({name: /^Max/})` finds all documents in the collection `coll` where the value of the `name` field starts with the string "Max".

In this query, the `/^Max/` portion is a regular expression (or regex) pattern enclosed in forward slashes (/). The `^` character inside the pattern means "start of string", so the pattern `/^Max/` will match any string that starts with "Max". The query searches for documents where the value of the `name` field matches this pattern.

For example, if the `coll` collection contains documents with the following `name` values:

db.coll.insertMany(\[{name: "Max Smith"},

{name: "Maxwell Johnson"},

{name: "Jessica Maxwell"}

\])

The query `db.coll.find({name: /^Max/})` would match the first two documents, but not the third one.

the output of the code here showed all the name fields with 'Max' in the database

{ \_id: ObjectId("64401d39484915799d73c26d"), name: 'Max' }

{ \_id: ObjectId("64401d4a484915799d73c26e"), name: 'Max' }

{ \_id: ObjectId("6440201e484915799d73c274"), name: 'Max' }

{ \_id: ObjectId("64403b99484915799d73c29e"), name: 'Max Smith' }

{ \_id: ObjectId("64403b99484915799d73c29f"), name: 'Maxwell Johnson' }