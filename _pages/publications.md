---
title: "Intemnets Lab - Publications"
layout: gridlay
excerpt: "Intemnets Lab -- Publications"
sitemap: false
permalink: /publications/
---

<br>
<h4><b>Here is our full list of <a href="#journalpubs">journal</a> and <a href="#confpubs">conference</a> publications.</b></h4>

<a name="journalpubs"> </a><br>
<h4>Journal Publications</h4>

{% assign number_printed = 1 %}
{% for publi in site.data.journalpubs %}
<br>
<b>[{{ number_printed }}] </b>
<b>{{ publi.title }}</b> <br /><em>{{ publi.authors }} </em><br /><a href="{{ publi.link.url }}">{{ publi.link.display }}</a><br>
<img src="{{ site.url }}{{ site.baseurl }}/images/pubpic/journalpics/{{ publi.image }}" style="width: 210px">
{% assign number_printed = number_printed | plus: 1 %}
{% endfor %}

<br>
<a name="confpubs"> </a>
<h4>Conference Publications</h4>

{% for publi in site.data.confpubs %}
<br>
<b>[{{ number_printed }}] </b>
<b>{{ publi.title }}</b> <br /><em>{{ publi.authors }} </em><br /><a href="{{ publi.link.url }}">{{ publi.link.display }}</a><br>
<img src="{{ site.url }}{{ site.baseurl }}/images/pubpic/confpics/{{ publi.image }}" style="width: 210px">
{% assign number_printed = number_printed | plus: 1 %}
{% endfor %}

<!--
<h3>Journal Publications</h3>

{% assign number_printed = 0 %}
{% for publi in site.data.journalpubs %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if publi.highlight == 1 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
 <div class="well">
  <pubtit>{{ publi.title }}</pubtit>
  <img src="{{ site.url }}{{ site.baseurl }}/images/pubpic/{{ publi.image }}" class="img-responsive" width="33%" style="float: left" />
  <p>{{ publi.description }}</p>
  <p><em>{{ publi.authors }}</em></p>
  <p><strong><a href="{{ publi.link.url }}">{{ publi.link.display }}</a></strong></p>
  <p class="text-danger"><strong> {{ publi.news1 }}</strong></p>
  <p> {{ publi.news2 }}</p>
 </div>
</div>

{% assign number_printed = number_printed | plus: 1 %}

{% if even_odd == 1 %}
</div>
{% endif %}

{% endif %}
{% endfor %}

<br>
<h3>Conference Publications</h3>

{% assign number_printed = 0 %}
{% for publi in site.data.conferencepubs %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if publi.highlight == 1 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
 <div class="well">
  <pubtit>{{ publi.title }}</pubtit>
  <img src="{{ site.url }}{{ site.baseurl }}/images/pubpic/{{ publi.image }}" class="img-responsive" width="33%" style="float: left" />
  <p>{{ publi.description }}</p>
  <p><em>{{ publi.authors }}</em></p>
  <p><strong><a href="{{ publi.link.url }}">{{ publi.link.display }}</a></strong></p>
  <p class="text-danger"><strong> {{ publi.news1 }}</strong></p>
  <p> {{ publi.news2 }}</p>
 </div>
</div>

{% assign number_printed = number_printed | plus: 1 %}

{% if even_odd == 1 %}
</div>
{% endif %}

{% endif %}
{% endfor %}
-->