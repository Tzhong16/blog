---
title: 'jQuery Event Handling'
layout: post
date: 2019-07-09 08:44
# image: /assets/images/markdown.jpg
headerImage: false
tag:
    - fontend
    - jQuery
# star: true
category: archive
archives: true
author: terence
description: jQuery Event Handling
---

### Major event type in jQuery
----

- Mouse Event
- Keyboard Event
- Form Event

![][/assets/images/post/keyboardandformevent.png]
<figcaption class="caption">Keyboard and Form Event</figcaption>

![][/assets/images/post/mouseevent.png]
<figcaption class="caption">Mouse Event</figcaption>



### Event delegation
----

  {% highlight html %}
   $(document).on('click', 'button', function(){
       // some code ... 
   })
  
  // normall way to handle event
  $(document).find('.button').on('click', function(){
       // some code 
  })
  {% endhighlight %}


