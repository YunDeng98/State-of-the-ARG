---
layout: single
title: "Upcoming Seminars"
permalink: /upcoming/
author_profile: false
classes: wide
---

Seminars take place on **Wednesdays at 08:30 PT / 11:30 ET / 16:30 UK time** during the academic year, from roughly September through June. Below is the full schedule for upcoming seminars.

If you would like to present your work in a future public **STATE OF THE <span style="color:#1c75bc;">ARG</span>** seminar, please complete this [Google Form](https://docs.google.com/forms/d/e/1FAIpQLSercPdrk5XhzL8M5shcO3F2AKcrLVv9OTpc7nbnynP0_cjQbw/viewform?usp=dialog). We welcome talks on methodological and empirical advances related to ancestral recombination graphs, population genomics, statistical genetics, evolutionary genetics, and related topics.

{% assign sorted_seminars = site.data.seminars | sort: "date" %}
{% assign today = "now" | date: "%Y%m%d" | plus: 0 %}
{% for seminar in sorted_seminars %}
{% assign seminar_date = seminar.date | date: "%Y%m%d" | plus: 0 %}
{% if seminar_date >= today %}
{% include seminar.html seminar=seminar next_up=sorted_seminars.first %}
{% endif %}
{% endfor %}
