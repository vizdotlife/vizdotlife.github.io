---
layout: page
title:  Blog
permalink: /blog/
image: '/images/photography/cnfts/VizDotLifePhotographySeriesOne0001resized_25.jpg'
---
TBD...

## Blog

{% assign sorted_posts = site.posts | sort:"num" %}
{% for post in sorted_posts %}
  {% if post.newest_tags contains 'collection' %}
    {% include new_article.html %}
  {% endif %}
{% endfor %}
