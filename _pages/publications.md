---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
---

{% if author.googlescholar %}
  You can also find my articles on <u><a href="{{author.googlescholar}}">my Google Scholar profile</a>.</u>
{% endif %}

{% include base_path %}

<p style="font-size:0.85em"><i>Journal quartiles: SCImago Journal Rank 2025. Impact factors: Journal Citation Reports 2025 (released 2026).</i></p>

{% for post in site.publications reversed %}
  {% include archive-single.html %}
{% endfor %}
