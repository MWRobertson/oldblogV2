---
layout: default
---

{% assign user = site.github.owner %}

{% for post in site.posts %}

## {{ post.title }}
{{ post.date }}

{{ post.content }}
* * *

{% endfor %}