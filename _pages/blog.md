---
layout: archive
title: Blogs
permalink: /blog/
excerpt: "Here are all your blogs."
header:
  overlay_image: /assets/images/hero_image.jpg
  overlay_filter: 0.7
  caption: "Photo credit: [**Unsplash**](https://unsplash.com)"
---

<h3 class="archive__subtitle">{{ site.date.ui-text[site.locale].recent_posts | default: "Recent Posts" }}</h3>

{% if paginator %}
    {% assign posts = paginator.posts %}
{% else %}
    {% assign posts = site.posts %}
{% endif %}

{% assign entries_layout = page.entries_layout | default: 'list' %}
<div class="entries-{{ entries_layout }}">
    {% for post in posts %}
        {% include archive-single.html type=entries_layout %}
    {% endfor %}
</div>

{% include paginator.html %}