---
title: 'CSS Positioning'
layout: post
date: 2019-07-14 08:44
# image: /assets/images/markdown.jpg
headerImage: false
tag:
    - fontend
    - CSS
# star: true
category: archive
archives: true
author: terence
description: CSS positioning
comments: true
---

## Display vs Postion

Block and inline are common value of display property. The block elements normally stack to each other, while inline elemnts won't flow downward to new line if there is enough space.

Position property determine the reference substance (参照物) of an element's position.

1. Static position

The default value for all elements.

2. Absolute position

Remove the element from the flow of document and move position based on the body element.

When an absolute element(a) wrap in a fixed/absolute/relative div/other element(b), then a will positioning bases on the b element (a's parent) instead of the body element.

![][3]


{% highlight css %}

.blueBox {
background: #627da0;
position: absolute;
left: 50px;
top: 50px;
}

.greenBox {
background: #5b8054;
}

.container {
background-color: rgba(168, 184, 28, 0.288);
width: 200px;
height: 200px;
position: relative;

top: 15px;
left: 100px;
}
    {% endhighlight %}

3. Fixed position

Remove the element from the flow of document and move position based on the window obj.

4. Relative position

The position of element will be maintain and the element will moving base on the original position.

5. Inherit

Child element will inherit the position property of parent. Also, when its parent has relative position, the child element will position base on the parent position.

<!-- ![][2] -->

{% highlight css %}

.blueBox {
background: #627da0;
position: inherit;
left: 50px;
top: 50px;
}

.container {
background-color: rgba(168, 184, 28, 0.288);
width: 200px;
height: 200px;
position: relative;
top: 15px;
left: 100px;
}
    {% endhighlight %}

> top, button, left, right only work for element with absolute or fixed or relative position.

## Float property

Float property will remove element from the flow of the document, and put it into far left or right, but the other elements still response the width and height or the float element.

1.  float: left/right

2.  clear: both/left/right

## Z-index property

Z-index property only effect when the elements have position property.

## Centering an element

1. Center horizontally

-   Method 1 (sigle elment)

{% highlight css %}

margin: 0 auto;
   {% endhighlight %}

-   Method 2 (multiple element)

{% highlight css %}
.blueBox {
background: #627da0;
}

.greenBox {
background: #5b8054;
}

.container div {
display: inline-block;
}

.container {
text-align: center;
}
    {% endhighlight %}

2. Center vertically and horizontally

{% highlight css %}
.box {
width: 100px;
height: 100px;
margin-right: 10px;
}

.blueBox {
margin: 0 auto;
}

/_ As the bluebox has a fixed width, inorder to horizontal the element we need the parent element to control the vertical position and give it 100% width _/

.container {
position: absolute;
top: 50%;
margin-top: -50px;
width: 100%;
left: 0;
margin-right: 10px;
}
    {% endhighlight %}

[1]: ../assets/images/post/displayandvisibility.png
[2]: ../assets/images/post/inherit-relative.png
[3]: ../assets/images/post/absolute-in-an-element.png
