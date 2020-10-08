---
layout: default
---

{% assign user = site.github.owner %}

{% for post in site.posts %}

## [{{ post.title }}]({{ post.url }})
{{ page.date | date: '%B %d, %Y' }}

{{ post.content }}
* * *

{% endfor %}