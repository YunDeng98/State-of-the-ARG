---
layout: single
permalink: /
author_profile: false
classes: wide
---

<div class="home-logo">
  <img src="{{ '/assets/images/state_of_the_arg_color_v4.png' | relative_url }}"
       alt="State of the ARG">
</div>

**STATE OF THE <span style="color:#1c75bc;">ARG</span>** is an online seminar series on advances in computational population genomics, with a particular focus on Ancestral Recombination Graphs (ARGs). The series brings together researchers developing new computational and statistical methods and applying them to questions in population genetics, statistical genetics, evolutionary biology, and related fields.

Seminars take place on **Wednesdays at 08:30 PT / 11:30 ET / 16:30 UK time** during the academic year, from roughly September through June. Our next seminar will be...

{% assign sorted_seminars = site.data.seminars | sort: "date" %}
{% assign today = "now" | date: "%Y%m%d" | plus: 0 %}
{% for seminar in sorted_seminars %}
{% if sorted_seminars.first %}
  {% assign seminar_date = seminar.date | date: "%Y%m%d" | plus: 0 %}
  {% if seminar_date >= today %}
  {% include seminar.html seminar=seminar next_up=sorted_seminars.first %}
  {% endif %}
{% endif %}
{% endfor %}

Please see the [Upcoming Seminars](/State-of-the-ARG/upcoming/) page for the full schedule of upcoming talks.

<br>

<h1>About this seminar series</h1>

**STATE OF THE <span style="color:#1c75bc;">ARG</span>** was initially established by core developers of [tskit](https://tskit.dev/) as a forum for exchanging ideas and discussing advances in genealogical methods for population genomics. It has since grown into a broader seminar series bringing together researchers developing and applying ARG-based methods.

**STATE OF THE <span style="color:#1c75bc;">ARG</span>** seminars have two formats: **public seminars** and **internal meetings**. Public seminars are open to everyone and are announced on this website; upcoming talks can be found on the [Upcoming Seminars](/State-of-the-ARG/upcoming/) page. Internal meetings are intended for members of the **STATE OF THE <span style="color:#1c75bc;">ARG</span>** community and provide a more informal setting for discussing ongoing work. Recordings of internal meetings may be made publicly available afterward with the speaker's consent. Information about previous seminars can be found on the [Previous Seminars](/State-of-the-ARG/previous/) page.

Origin of the name: The name **STATE OF THE <span style="color:#1c75bc;">ARG</span>** originated from a comment by Prof. Moi Exposito-Alonso during Yun Deng's exit talk at the UC Berkeley Center for Theoretical Evolutionary Genomics (CTEG).

<br>

<h1>Interested in presenting?</h1>

If you would like to present your work in a future public **STATE OF THE <span style="color:#1c75bc;">ARG</span>** seminar, please complete this [Google Form](https://docs.google.com/forms/d/e/1FAIpQLSercPdrk5XhzL8M5shcO3F2AKcrLVv9OTpc7nbnynP0_cjQbw/viewform?usp=dialog). We welcome talks on methodological and empirical advances related to ancestral recombination graphs, population genomics, statistical genetics, evolutionary genetics, and related topics.
