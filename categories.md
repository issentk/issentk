---
layout: static
---

# Categories

Please find a list of the posts sorted by categories below or <a href="{{ site.baseurl }}/index.html">go back</a>.

{% for category in site.categories %}
  {% assign cat = category[0] %}
  <h2 id="{{ cat | slugify }}">{{ cat }}</h2>
  <ul>
   {% for post in site.posts %}
     {% if post.categories contains cat %}
     <li>
     <div>
     <a href="{{ post.url }}">
     {{ post.title }}
     <small class="small-date">{{ post.date | date_to_long_string }}</small>
     </a>
     </div>
     </li>
     {% endif %}
   {% endfor %}
  </ul>
{% endfor %}
