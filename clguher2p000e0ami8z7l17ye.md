---
title: "Learn CSS  POSITIONING PROPERTY(Relative Static and absolute positions)"
seoTitle: "CSS POSITIONING PROPERTY"
seoDescription: "The relative the position value is used to position an element relative to its normal position within the document flow. When an element is given a position"
datePublished: Mon Apr 24 2023 06:53:10 GMT+0000 (Coordinated Universal Time)
cuid: clguher2p000e0ami8z7l17ye
slug: learn-css-positioning-propertyrelative-static-and-absolute-positions
cover: https://cdn.hashnode.com/res/hashnode/image/stock/unsplash/bKjHgo_Lbpo/upload/d2fa6a73f5d5b058139dcbd775d0b14e.jpeg
tags: static, position-relative, css-positioning-property, absolute-position

---

The `relative` the position value is used to position an element relative to its normal position within the document flow. When an element is given a `position: relative` property, it can be moved from its original position by specifying a top, bottom, left, or right value. Other elements on the page will continue to flow as if the positioned element were in its normal position.

The `static` value is the default value for the `position` property and it means that the element is positioned according to the normal document flow.

The `absolute` value positions an element relative to its nearest positioned ancestor element, or to the document body if no ancestor elements are positioned.

The `fixed` value positions an element relative to the viewport, which means it will always stay in the same position even if the page is scrolled.

&lt;div class="container"&gt;

&lt;div class="box"&gt;&lt;/div&gt;

&lt;/div&gt;

.container { position: relative; }

.box { position: absolute; top: 50px; left: 50px; }

In this example, the `.container` element is set to `position: relative`, which makes it the "anchor" for the absolutely positioned `.box` element. The `.box` element is then positioned `50px` from the top and `50px` from the left of the `.container` element.