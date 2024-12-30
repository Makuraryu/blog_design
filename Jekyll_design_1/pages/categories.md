---
layout: default
title: 分类
description: 本博客所有文章分类列表。
keywords: 分类
permalink: /categories/
---
<div class="categories">

{% for category in site.categories %}

<p class="category">{{ category[0] }}({{ category[1].size }})</p>

{% for post in category.last %}
  <p>
    <a class="catposts" href="{{ site.url }}{{ post.url }}">
    {{ post.title }}
    </a>
  </p>
{% endfor %}

{% endfor %}
</div>
