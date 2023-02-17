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
  <p class="bigger-text">Date: February 15th 2023</p>
  <p class="bigger-text">Time: 2PM-4PM</p>
  <p class="bigger-text">Location: </p> 
  <p>  Location: <a href="https://www.u-paris2.fr/fr/recherche/centres-de-recherche/implantations/centre-de-recherche-en-economie-et-droit-cred"> CRED </a>, 21 Rue Valette, 75005 Paris.  </p> 
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
      <h1 style="margin: 0;">
        {% if intervention.presenter.url %}
          <a href="{{ intervention.presenter.url }}">{{ intervention.presenter.name }}</a>
        {% else %}
          {{ intervention.presenter.name }}
        {% endif %}
      </h1>
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
