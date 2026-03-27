---
layout: inner
title: "Research"
subtitle: "Peer-reviewed publications in healthcare analytics, optimization, and AI."
permalink: /research/
redirect_from:
  - /publications/
---

{% include base_path %}

{% if site.author.googlescholar %}
You can also find my articles on <a href="{{ site.author.googlescholar }}">my Google Scholar profile</a>.
{% endif %}

{% for post in site.publications reversed %}
  {% include archive-single.html %}
{% endfor %}
