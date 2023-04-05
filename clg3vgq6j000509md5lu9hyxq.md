---
title: "insertion and deletion in an array using the heap method"
seoTitle: "insertion and deletion in an array using the heap method"
seoDescription: "//Insertion in a max heap

function insertionInAHeap(arr, key){

  arr.push(key)

   let firstNonLeafNodeIdx = Math.floor((arr.length) / 2) - 1

  for(let i"
datePublished: Wed Apr 05 2023 15:56:50 GMT+0000 (Coordinated Universal Time)
cuid: clg3vgq6j000509md5lu9hyxq
slug: insertion-and-deletion-in-an-array-using-the-heap-method
cover: https://cdn.hashnode.com/res/hashnode/image/stock/unsplash/xG8IQMqMITM/upload/78db8202706b6d47ffcaf943a84096f3.jpeg
tags: array, insertion, deletions

---

//Insertion in a max heap

function insertionInAHeap(arr, key){

  arr.push(key)

   let firstNonLeafNodeIdx = Math.floor((arr.length) / 2) - 1

  for(let i = firstNonLeafNodeIdx; i &gt;= 0; i--){

      heapify(arr, i)

  }

}

//Deletion in a max heap

function deletionInAHeap(arr){

  let firstElement = arr\[0\]

  let lastElement = arr.pop()

  arr\[0\] = lastElement

  heapify(arr, 0)

return firstElement

}

function heapify(arr, i){

  let largestIdx = i

  let leftChildIdx = 2 \* i + 1

  let rightChildIdx = 2 \* i + 2

   if(leftChildIdx &lt; arr.length && arr\[leftChildIdx\] &gt; arr\[largestIdx\]){

    largestIdx = leftChildIdx

  }

  if(rightChildIdx &lt; arr.length && arr\[rightChildIdx\] &gt; arr\[largestIdx\]){

    largestIdx = rightChildIdx

  }

if(largestIdx != i){

    let temp = arr\[i\]

    arr\[i\] = arr\[largestIdx\]

    arr\[largestIdx\] = temp

    //Call heapify again on the swapped index

    heapify(arr, largestIdx)

  } 

}

//Invoke

let arr = \[4, 9, 11, 3, 2, 17\]

insertionInAHeap(arr, 21)

console.log(arr)

deletionInAHeap(arr)

console.log(arr)