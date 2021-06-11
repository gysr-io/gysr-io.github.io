---
layout: page
---

*This documentation describes the functionality and interface for the **GYSR Core v2** contracts.
The associated source code can be found at [github.com/gysr-io/core](https://github.com/gysr-io/core)*

{% for page in site.pages %}
{%- if page.categories contains 'contract' -%}

<div>

<a href="{{page.url}}">{{page.title}}</a>
<br>
<small> {{page.description}}</small>
</div>

{%- endif -%}
{% endfor %}
