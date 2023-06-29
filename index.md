---
layout: default
title: Presentations
---

By [Haroen Viaene](https://haroen.me)

Talks and presentations done in recent times.

{% assign talks = site.pages | sort: "date" | reverse %}

- 🇬🇧

  <ul>
  {% for talk in talks %}
  {% assign dir = talk.dir | split: "/" %}
  {% if dir[1] == "en" %}
  <li><a href=".{{ talk.url }}">{{ talk.title }}</a> ({{ talk.date | date: "%Y-%m-%d" }})</li>
  {% endif %}
  {% endfor %}
  </ul>

- 🇫🇷

  <ul>
  {% for talk in talks %}
  {% assign dir = talk.dir | split: "/" %}
  {% if dir[1] == "fr" %}
  <li><a href=".{{ talk.url }}">{{ talk.title }}</a> ({{ talk.date | date: "%Y-%m-%d" }})</li>
  {% endif %}
  {% endfor %}
  </ul>

# [CFPs](cfps)

Talks I haven't done yet or want to give again, if you're organising a conference or meetup, [📧 me](mailto:hello@haroen.me)
