---
layout: page
permalink: /publications/
title: Research
description: 
pubyears: [2021]
wpyears: [2019]
wipyears: []
nav: true
nav_order: 1
---
<!-- _pages/publications.md -->
<div class="publications">

<h3  class="wips">Work in Progress</h3>

  <h2 class="year"> . </h2>

  {% bibliography -f wip %}


<h3  class="wps">Working Papers</h3>

{%- for y in page.wpyears %}
  <h2 class="year">{{y}}</h2>
  {% bibliography -f wp -q @*[year={{y}}]* %}
{% endfor %}

<h3  class="pubs">Publications</h3>

{%- for y in page.pubyears %}
  <h2 class="year">{{y}}</h2>
   <!-- "papers" is .bib file-->
  {% bibliography -f pubs -q @*[year={{y}}]* %}
{% endfor %}


</div>

