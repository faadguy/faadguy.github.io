---
layout: default
title: Blog
---
<div class="container" style="padding-top:140px">
<h1 style="font-size:50px">Trending</h1>

{% for post in site.posts %}

{% if post.featured %}
  <div class="posts post-web" >


    <div class="post-title post-title-web" style="margin-bottom: 0rem;"><h1 style="font-weight:600;"><a href="{{ post.url }}">{{ post.title }}</a></h1><h3 style="font-size: 1.8rem;font-weight:300;">~ {{ post.date | date_to_string }}</h3></div>
    {% if post.description %}<p class="post-description post-description-web">{{ post.description }}<br><br><a href="{{ post.url }}"><u style="color:#313131">...Read more</u></a></p>{% endif %}

  </div>
  {% endif %}
{% endfor %}

<h1 style="font-size:50px; margin-top:40px;">All</h1>

{% for post in site.posts %}

{% if post.featured %}
{% else %}

  <div class="post post-web">



    <div class="post-title post-title-web" style="margin-bottom: 0rem;"><h1 style="font-weight:600;"><a href="{{ post.url }}">{{ post.title }}</a></h1><h3 style="font-weight:300;font-size:1.9rem;">~ {{ post.date | date_to_string }}</h3></div>
    {% if post.description %}<p class="post-description post-description-web">{{ post.description }}<br><br><a href="{{ post.url }}"><u>...Read more</u></a></p>{% endif %}


  </div>
  {% endif %}
{% endfor %}
</div>
