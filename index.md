---
layout: default
---

{% assign user = site.github.owner %}

{% for post in site.posts %}

## {{ post.title }}
{% assign d = page.date | date: "%-d"  %}
{{ page.date | date: "%B" }} 
{% case d %}
  {% when '1' or '21' or '31' %}{{ d }}st
  {% when '2' or '22' %}{{ d }}nd
  {% when '3' or '23' %}{{ d }}rd
  {% else %}{{ d }}th
  {% endcase %}, 
{{ page.date | date: "%Y" }}

{{ post.content }}
* * *

{% endfor %}