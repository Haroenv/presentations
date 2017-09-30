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
  <article id="{{page.title | downcase | replace: ' ', '-'}}" class="cfp">
    <a href="#{{page.title | downcase | replace: ' ', '-'}}">🔗</a>
    <details>
    <summary><h3>{{page.title}}</h3></summary>
    {{page.content | markdownify}}
    </details>
  </article>
  {% endif %}
{% endfor %}

<script>
  function openDetails() {
    const others = document.querySelectorAll('details');
    others.forEach(detail => detail.removeAttribute('open'));
    const details = document.querySelector(`${location.hash} details`);
    details.setAttribute('open', true);
  }
  window.addEventListener('hashchange', openDetails);
  openDetails();
</script>
