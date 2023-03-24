---
title: "WCSNG - Team"
layout: gridlay
excerpt: "WCSNG: Team members"
sitemap: false
permalink: /team/
---

# ECE257B Staff


<div class="row">
<div class="col-sm-6 clearfix">
  <img src="{{ site.url }}{{ site.baseurl }}/images/teampic/dinesh.jpg" class="img-responsive" width="32%" style="float: left" />
  <!-- <div class="col-sm-7 clearfix"> -->
  <h3>Dinesh Bharadia</h3>
  Principal Investigator, WCSNG<br>
  Associate Professor<br>
  Department of Electrical and Computer Engineering <br>
  University of California, San Diego
<ul style="margin: 0; padding: 0; list-style-type:none; overflow: hidden">
<li>Email: <b>dineshb [at] eng.ucsd.edu</b></li>
<li>Office: FAH 2303, Franklin Antonio Hall</li>
<li><a href="https://web.eng.ucsd.edu/~dineshb/"> Personal Website </a> | <a href="https://scholar.google.com/citations?user=5SjaXJsAAAAJ&hl=en"> Google Scholar </a></li>
</ul>

</div>

</div>


## TAs
{% assign number_printed = 0 %}
{% for member in site.data.ta2023 %}

{% assign even_odd = number_printed | modulo: 2 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
  <img src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ member.photo }}" class="img-responsive" width="25%" style="float: left" />
  <h4>{{ member.name }}</h4>
  <i>{{ member.info }}</i><br>{{ member.email }}
  <ul style="overflow: hidden">

  {% if member.number_educ == 1 %}
  <li> {{ member.education1 }} </li>
  {% endif %}

  {% if member.number_educ == 2 %}
  <li> {{ member.education1 }} </li>
  <li> {{ member.education2 }} </li>
  {% endif %}

  {% if member.number_educ == 3 %}
  <li> {{ member.education1 }} </li>
  <li> {{ member.education2 }} </li>
  <li> {{ member.education3 }} </li>
  {% endif %}

  {% if member.number_educ == 4 %}
  <li> {{ member.education1 }} </li>
  <li> {{ member.education2 }} </li>
  <li> {{ member.education3 }} </li>
  <li> {{ member.education4 }} </li>
  {% endif %}

  {% if member.number_educ == 5 %}
  <li> {{ member.education1 }} </li>
  <li> {{ member.education2 }} </li>
  <li> {{ member.education3 }} </li>
  <li> {{ member.education4 }} </li>
  <li> {{ member.education5 }} </li>
  {% endif %}

  </ul>
</div>

{% assign number_printed = number_printed | plus: 1 %}

{% if even_odd == 1 %}
</div>
{% endif %}

{% endfor %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if even_odd == 1 %}
</div>
{% endif %}

