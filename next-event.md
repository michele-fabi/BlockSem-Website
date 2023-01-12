---
layout: page
title: Next Seminar
permalink: /
---

<style>
  .presenter-image {
    margin-right: 1em;
  }
</style>



<div class="upcoming-event-page">

  <div class="event-info">
  <p class="bigger-text">Date: January 25th 2023</p>
  <p class="bigger-text">Time: 2PM-4PM</p>
  <p class="bigger-text">Location: </p> 
  <p>  LIP6, Sorbonne University (Pierre and Marie Curie Campus) - 4 place Jussieu (metro Jussieu), tower 26, first flour, hall 25-26, room 105.  </p> 
  <p>  The room can be accessed either via tower 26 or via tower 25 (https://www.lip6.fr/informations/comment.php). </p>
  </div>  

  {% assign sorted_interventions = site.home-interventions | sort: 'order' %}
  {% for intervention in sorted_interventions %}
  
  {% if intervention.order == 1 %}
    <h3>First Presentation:</h3>
  {% endif %}
  {% if intervention.order == 2 %}
    <h3>Second Presentation:</h3>
  {% endif %}
  
      <div class="intervention">
<div class="presenter-info-home">
  <div class="presenter-name-and-affiliation">
    <h1 style="margin: 0;"><a href="{{ intervention.presenter.url }}">{{ intervention.presenter.name }}</a></h1>
    <h3 style="margin: 0 auto 20px auto; padding: 0;">({{ intervention.presenter.affiliation }})</h3>
  </div>
  
  <img src="{{ intervention.presenter.image  | relative_url }}" alt="{{ intervention.presenter.name }}" class="bigger-image">
</div>
        <h2 class="italicized-title">{{ intervention.title }}</h2>
        <h3> Abstract: </h3>
        <div class="intervention-abstract">{{ intervention.abstract | markdownify  }}</div>
      </div>
      <hr />
  {% endfor %}
</div>
