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
    {% highlight css %}
    div p {
    background-color:#ddddaa;
    }
    {% endhighlight %}

-   Child selector
    {% highlight css %}
    div > p{
    background-color: #ddddaa;
    }
    {% endhighlight %}

-   Attribute selector
    {% highlight css %}
    img[alt=spacer]{
    padding:0px;
    }
    {% endhighlight %}

-   Psuedo class
    {% highlight css %}
    a:visited {
    color: #dddddd;
    }
    {% endhighlight %}

### Property values

### Ordering Rules

    !important >inline > id > class 后(in style) >class 前> body > :root

## Specificity

![][1]

### Inheritance

The parent style will flow through to their children, when mean children node will inheritance all the style from their parent.

Note that not every property can be inheritable, such as `border, margins, padding`. And most font-related and listed related properties are inheritable. Like `front-size, font family`.

### Style sheet priority from different sources

    Author stylesheets > User stylesheet > default stylesheet

## Border, Margin, Padding

![][2]

 <figcaption class="caption">Box model</figcaption>

## Vertical margins collapse

> Horizontally margins do not collapse

When top and bottom margins meet, they will overlap. This only happen in vertical margins. Which mean horizontally margins do not apply.

![][3]

<figcaption class="caption">Margins Overlap</figcaption>

[1]: ../assets/images/post/specificity.png
[2]: ../assets/images/post/boxmodel.png
[3]: ../assets/images/post/maginsoverlap.png
