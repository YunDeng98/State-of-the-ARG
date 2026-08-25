---
layout: single
title: "State of the ARG"
permalink: /
author_profile: false
classes: wide
---

State-of-the-ARG is an online seminar series covering methodological developments and applications of ancestral recombination graphs (ARGs). It is the successor to the tskit online seminar series.

Talks are held online and are open to everyone.

## Upcoming Seminars

{% assign sorted_seminars = site.data.seminars | sort: "date" %}
{% assign current_date = "now" | date: "%Y%m%d" | plus: 0 %}

{% for seminar in sorted_seminars %}
{% assign seminar_date = seminar.date | date: "%Y%m%d" | plus: 0 %}
{% if seminar_date >= current_date %}
{% include seminar.html %}
{% endif %}
{% endfor %}
