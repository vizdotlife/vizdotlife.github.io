---
layout: page
title:  Blog
permalink: /my-blog/
image: '/images/photography/cnfts/VizDotLifePhotographySeriesOne0001resized_25.jpg'
---
TBD...

## Blog
Coming soon...

<div class="container">
  <h1>{{ "Hello World!" | downcase }}</h1>
  <div class="row animate">
    {% assign sorted_posts = site.posts | sort:"num" %}
    {% for post in sorted_posts %}
      {% if post.newest_tags contains 'collection' %}
        {% include new_article.html %}
      {% endif %}
    {% endfor %}
  </div>
</div>

{% include pagination.html %}
