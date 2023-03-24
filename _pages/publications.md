---
title: "WCSNG - Publications"
layout: gridlay
excerpt: "WCSNG -- Publications."
sitemap: false
permalink: /publications/
---


# Publications

## Highlights

For a full list see [below](#full-list) or go to [Google Scholar](https://scholar.google.com/citations?hl=en&user=5SjaXJsAAAAJ&view_op=list_works&sortby=pubdate), and [DBLP](http://dblp.uni-trier.de/pers/hd/b/Bharadia:Dinesh).

Please go to [Research]({{ site.url }}{{ site.baseurl }}/research) section for category-wise list of papers.

{% assign number_printed = 0 %}
{% for publi in site.data.publist %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if publi.highlight == 1 %}

{% if even_odd == 0 %}

<div class="row">
{% endif %}


<div class="col-sm-13 clearfix">
 <div class="well">
  <pubtit>{{ publi.title }} <a href="{{ publi.link.url }}"><span style="color:tomato;">{{ publi.link.display }}</span></a></pubtit>
  <p><strong>
  <a href="{{ publi.website.url }}">{{ publi.website.display }}</a>
  <a href="{{ site.url }}{{ site.baseurl }}/{{ publi.paper.url }}"><span style="color:#D35400;">{{ publi.paper.display }}</span></a>
  <a href="{{ site.url }}{{ site.baseurl }}/{{ publi.presentation.url }}"><span style="color:#7D3C98;">{{ publi.presentation.display }}</span></a> 
  </strong></p>
  <p><em>{{ publi.authors }}</em></p>
  
  <meta name="publi.keywords.name" content="{{ publi.keywords.content }}">
  <img src="{{ site.url }}{{ site.baseurl }}/images/pubpic/{{ publi.image }}" class="img-responsive" width="50%" style="float: left" hspace="20" />
  <p>{{ publi.description }}</p>
  <p class="text-danger"><strong> {{ publi.news1 }}</strong></p>
  <p> {{ publi.news2 }}</p>
 </div>
</div>

<!--
 <div class="col-sm-12 clearfix">
  <div class="well">
  <pubtit>{{ publi.title }}</pubtit>
  <p><strong><a href="{{ publi.website.url }}">{{ publi.website.display }}</a></strong></p>
  <meta name="publi.keywords.name" content="{{ publi.keywords.content }}">
  <img src="{{ site.url }}{{ site.baseurl }}/images/pubpic/{{ publi.image }}" class="img-responsive" width="50%" style="float: left" />
  <p>{{ publi.description }}</p>
  <p><em>{{ publi.authors }}</em></p>
  <p><strong><a href="{{ publi.link.url }}">{{ publi.link.display }}</a></strong></p>
  <p class="text-danger"><strong> {{ publi.news1 }}</strong></p>
  <p> {{ publi.news2 }}</p>
 </div>
</div>
-->
{% assign number_printed = number_printed | plus: 1 %}

{% if even_odd == 1 %}
</div>
{% endif %}

{% endif %}
{% endfor %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if even_odd == 1 %}
</div>
{% endif %}

<p> &nbsp; </p>


## Full List

{% for publi in site.data.publist %}

  {{ publi.title }} <br />
  <em>{{ publi.authors }} </em><br /><a href="{{ publi.link.url }}">{{ publi.link.display }}</a>

{% endfor %}

