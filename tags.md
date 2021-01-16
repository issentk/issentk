---
layout: static
---

# Tags

Please find a list of the posts sorted by source tags below or <a href="{{ site.baseurl }}/index.html">go back</a>.

{% for tag in site.tags %}
  {% assign t = tag[0] %}
  <h2 id="{{ t | slugify }}">{{ t }}</h2>
  <ul>
   {% for post in site.posts %}
     {% if post.tags contains t %}
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
