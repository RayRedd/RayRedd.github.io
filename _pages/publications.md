---
layout: archive
title: "Publications"
permalink: /publications
author_profile: true
---

{% if author.googlescholar %}
  You can also find my articles on <u><a href="{{author.googlescholar}}">my Google Scholar profile</a>.</u>
{% endif %}

{% include base_path %}

<h1>Journals</h1>
{% for post in site.publications %}
  {% if post.type contains "journal" %}
    {% include archive-single.html %}
  {% endif %}
{% endfor %}


<h1>Conference</h1>
{% for post in site.publications %}
  {% if post.type contains "conference" %}
    {% include archive-single.html %}
  {% endif %}
{% endfor %}

<h1>Invited paper</h1>
{% for post in site.publications %}
  {% if post.type != 'journal' and post.type != 'conference' %}
    {% include archive-single.html %}
  {% endif %}
{% endfor %}
