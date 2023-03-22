---
title: "What is the Difference between the positions Realtive and Absolute"
datePublished: Mon Feb 06 2023 07:56:40 GMT+0000 (Coordinated Universal Time)
cuid: cldsirtja000f09i9gjfd3ra9
slug: what-is-the-difference-between-the-positions-realtive-and-absolute
cover: https://cdn.hashnode.com/res/hashnode/image/stock/unsplash/vcF5y2Edm6A/upload/ef95ae3c77e030ca19f5a056c4ffd8cc.jpeg
tags: css, animation, position, position-relative, position-property-in-css

---

The main difference between position: relative and position: absolute is how they are positioned in relation to their parent container and the other elements on the page.

* When an element has a position: relative, it is positioned relative to its normal position, and you can use the top, right, bottom, and left properties to move it away from that normal position. The element will still take up space in the normal flow of the document and affect other elements as if it were still in its normal position.
    
* When an element has a position: absolute, it is taken out of the normal flow of the document and positioned relative to its nearest positioned ancestor (or the body if none is found), if no positioned ancestor is found, the element will be positioned relative to the initial containing block (usually the body itself). The element will not affect other elements on the page and will not take up any space.
    

In summary, position: relative is used to creating an offset from an element's default position, whereas position: absolute is used to create an element that is taken out of the normal flow of the document and is positioned relative to its nearest positioned ancestor.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1675670083895/738e4921-4dc9-487e-98d9-b860c3e52325.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1675670107923/437f65bb-a4c2-4dfb-a7c4-854064cccd1e.png align="center")