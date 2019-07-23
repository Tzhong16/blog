---
title: 'jQuery DOM Manipulation'
layout: post
date: 2019-07-10 08:44
# image: /assets/images/markdown.jpg
headerImage: false
tag:
    - fontend
    - jQuery
# star: true
category: archive
archives: true
author: terence
description: jQuery DOM Manipulation
comments: true
---

### DOM’s element manipulation in jQuery

-   append( )
-   prepend( )
-   after( )
-   before( )

### DOM’s class manipulation in jQuery

-   addClass( )
-   removeClass( )
-   toggleClass( )
-   hasClass( )

### DOM’s CSS manipulation in jQuery

-   css( )

    {% highlight html %}
    \$(this).find('.price').css('dispaly', 'block')

    \$(this).find('.price').css({'background-color': '#252b30', 'border-color': '1px solid #967'})
    {% endhighlight %}

-   animate( )

    animate method can manager css style form current sytle to other sytle

{% highlight html %}
if(<vacation has the class highlighted>){
$(this).animate({'top':'-10px'})
}else{
$(this).animate({'top':'0px'})
}
{% endhighlight %}

### 'this' in jQuery and data()

-   `this` in jQuery should wrap in \$(), then the element will convert to jQuery object

-   data( )
    Use when you want to get the custom attribute value from element

{% highlight javascript %}
// assume custom attribute is data-US = "200"
// the + sign is used to convert the value into number
const usValue= +("#destination").first().data('US')
{% endhighlight %}
