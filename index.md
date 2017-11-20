---
title: Study Math
---

{% for tag in site.categories %} 
<h2 id="{{ tag[0] }}">{{ tag[0] | capitalize }}</h2>
<ul class="post-list">{% assign pages_list = tag[1] %}{% for post in pages_list %}{% if post.title != null %}{% if group == null or group == post.group %}
  <li><a href="{{ site.url }}{{ post.url }}">{{ post.title }}</a></li>
  {% endif %}{% endif %}{% endfor %}
  </ul>{% assign pages_list = nil %}{% assign group = nil %}
{% endfor %}

<h2 id="otherlinks">Other links</h2>
<ul class="post-list">
  <li><a href="https://philosophicalmath.wordpress.com/">Philosophical Math</a></li>
</ul>
