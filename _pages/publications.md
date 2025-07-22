---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
---
{% include base_path %}

## 🧪 Journal Articles
{% assign journal_pubs = site.publications | where: "category", "journal" | sort: "date" | reverse %}
{% for post in journal_pubs %}
  {% include archive-single-publication.html %}
{% endfor %}

## 🧠 Conference Papers / Abstracts
{% assign conf_pubs = site.publications | where: "category", "conference" | sort: "date" | reverse %}
{% for post in conf_pubs %}
  {% include archive-single-publication.html %}
{% endfor %}


{% comment %}
{% if author.googlescholar %}
  You can also find my articles on <u><a href="{{author.googlescholar}}">my Google Scholar profile</a>.</u>
{% endif %}

{% include base_path %}

{% for post in site.publications reversed %}
  {% include archive-single.html %}
{% endfor %}
{% endcomment %}
