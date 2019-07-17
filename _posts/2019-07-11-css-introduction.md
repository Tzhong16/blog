---
title: 'CSS Introduction'
layout: post
date: 2019-07-11 08:44
# image: /assets/images/markdown.jpg
headerImage: false
tag:
    - fontend
    - CSS
# star: true
category: archive
archives: true
author: terence
description: CSS introduction
comments: true
---

### Other selectors in CSS

-   Descendant selector
    {% highlight html %}
    div p {
    background-color:#ddddaa;
    }
    {% endhighlight %}

-   Child selector
    {% highlight html %}
    div > p{
    background-color: #ddddaa;
    }
    {% endhighlight %}

-   Attribute selector
    {% highlight html %}
    img[alt=spacer]{
    padding:0px;
    }
    {% endhighlight %}

-   Psuedo class
    {% highlight html %}
    a:visited {
    color: #dddddd;
    }
    {% endhighlight %}

### Property values

### Ordering Rules

    !important >inline > id > class 后(in style) >class 前> body > :root

### Inheritance

The parent style will flow through to their children, when mean children node will inheritance all the style from their parent.

Note that not every property can be inheritable, such as `border, margins, padding`. And most font-related and listed related properties are inheritable. Like `front-size, font family`.

### Style sheet priority from different sources

    Author stylesheets > User stylesheet > default stylesheet

## Border, Margin, Padding

![][/assets/images/post/boxmodel.png]

 <figcaption class="caption">Box model</figcaption>

## Vertical margins collapse

    When top and bottom margins meet, they will overlap. This only happen in vertical margins. Which mean horizontally margins do not apply.

    ![][/assets/images/post/maginsoverlap.png]
            <figcaption class="caption">Margins Overlap</figcaption>

### Some tricks in CSS

-   Hide dot sign of unorder list

         {% highlight html %}
            ul{
                list-style-type: none;
                //or
                // list-style: none;
            }
          {% endhighlight %}

-   Width only apply to the `content` of the box

-   Some normal font family:

    1. serif (default, common in News post)
    2. sans-serif (common in most web content)
    3. monosplace (good for code website)
    4. arial

-   `text-decoration: none;` remove the underline of anchor elemnt

-   Display property
    Every HTML element has **display property**, the value can be set with `block, inline, none`.

    When use `display: inline;`, the width setting for each element wouldn't be affect. As we can't set width for inline elements (span, input). Instead, we can see `display: inline-block;` to solve the problem.

    ![][/assets/images/post/displayandvisibility.png]

    <figcaption class="caption">Display property</figcaption>

*   Display VS Visibility

    `display: none;` can remove all the whole element with its space and content.
    `visibility: hidden;` only hide the element but keep its space and content area.

*   Float and Clear
    `float` can stack the element in same line if there is enough room
    `clear` can remove the element floating to other element, common use is `clear: both;`
