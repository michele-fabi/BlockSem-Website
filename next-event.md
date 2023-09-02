---
layout: page
title: Next Seminar
permalink: /next
---

<style>
  .presenter-image {
    margin-right: 1em;
  }
</style>



<div class="upcoming-event-page">

  <div class="event-info">
  <p class="bigger-text"> Blocksem is looking for presenters for the academic year 2023/2024. If you are interested at presenting, please contact us.  </p>  
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
