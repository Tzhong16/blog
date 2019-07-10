---
title: 'jQuery Selector'
layout: post
date: 2019-07-08 08:44
# image: /assets/images/markdown.jpg
headerImage: false
tag:
    - fontend
    - jQuery
# star: true
category: archive
archives: true
author: terence
description: Introduction of jQuery selector
---

### CSS selector in jQuery

{% highlight raw %}
$("<id_name>") // by id
$("#destination")

$("<tag_name>") // by tag
$("li")

$("<class_name>") // by class
$(".prom")

{% endhighlight %}


### More complex CSS selector

1. Descendant selector 

{% highlight raw %}
// #destination is parent, li tag is descendant
//all li tags within #destination will show
$("#destination li")

{% endhighlight %}

2. Child selector

{% highlight raw %}
//Compare to descendant selector
$("#destination > li") //only direct child of destination will show
{% endhighlight %}

3. Multiple selector

{% highlight raw %}
$("#france, .promo") 
{% endhighlight %}

4. Pseudo selector

{% highlight raw %}
$("#destination li:first")
$("#destination li:last")
$("#destination li:odd")
$("#destination li:even")
{% endhighlight %}

<div class="breaker"></div>

### Traversing the DOM

> traversing the dom is a bit faster 

- find("css_selector_name")
- closest("css_selector_name")
- filter("css_selector_name")
- next( )
- prev( )
- parent( )
- parents( ) **#all parents**
- children( ) **#only direct children**
- data("css_selector_name") **#select custom attribute value**
- filter("css_selector_name") 