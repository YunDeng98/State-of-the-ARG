---
layout: single
title: "Previous Seminars"
permalink: /previous/
author_profile: false
classes: wide
---

{% assign sorted_seminars = site.data.seminars | sort: "date" | reverse %}
{% assign today = "now" | date: "%Y%m%d" | plus: 0 %}

{% for seminar in sorted_seminars %}
  {% assign seminar_date = seminar.date | date: "%Y%m%d" | plus: 0 %}
  {% if seminar_date < today %}
    {% include seminar.html seminar=seminar %}
  {% endif %}
{% endfor %}
