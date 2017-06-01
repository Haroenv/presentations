---
layout: default
---

<style>
summary h3{
  display: inline-block
}
</style>

# CFPs

[←](..)

Here I maintain my CFPs

{% for page in site.pages %}
  {% if page.type == 'cfp' %}
  <details>
  <summary><h3>{{page.title}}</h3></summary>
  {{page.content | markdownify}}
  </details>
  {% endif %}
{% endfor %}
