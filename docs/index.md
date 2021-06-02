---
layout: page
---

{% for page in site.pages %}
{%- if page.categories contains 'contract' -%}

<div>

<a href="{{page.url}}">{{page.title}}</a>
<br>
<small> {{page.description}}</small>
</div>

{%- endif -%}
{% endfor %}
