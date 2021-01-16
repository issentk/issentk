---
layout: static
---

# Archive

Please find a list of our blog posts below or <a href="{{ site.baseurl }}/index.html">go back</a>.
You can sort posts by [categories]({{site.baseurl}}categories.html) or [tags]({{site.baseurl}}tags.html).

{% for post in site.posts %}

<ul>
  <li>
  <div>
  <a href="{{site.baseurl}}{{ post.url }}">
  {{ post.title }}
  <small class="small-date">{{ post.date | date_to_long_string }}</small>
  </a>
  </div>
  </li>
</ul>

{% endfor %}
