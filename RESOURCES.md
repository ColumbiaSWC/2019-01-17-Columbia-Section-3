---
layout: page
title: Resources
permalink: resources.html
resources:
  - link: https://rcfoundations.research.columbia.edu/content/helpdesk
    label: Foundations for Research Computing Help Desk
---
<style>
  .resources {
    text-align:center;
    margin:0 auto;
  }
</style>

<div class='resources'>
  {% for r in page.resources %}
    <p><a href='{{ r.link }}'>{{ r.label }}</a></p>
  {% endfor %}
</div>
