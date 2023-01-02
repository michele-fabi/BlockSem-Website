---
layout: page
title: Past Seminars
permalink: /events/
---

<!-- _layouts/interventions.html -->

<style>
  .presenter-image {
    margin-right: 1em;
  }
</style>

<div class="interventions-page">
  {% assign sorted_interventions = site.interventions | sort: 'date' | reverse %}
  {% for intervention in sorted_interventions %}
    <div class="intervention">
		<div class="intervention-date">{{ intervention.date | date: "%d-%m-%Y" }}</div>
		<div class="intervention-title-and-links">
		  <h2 class="intervention-title">{{ intervention.title }}
		  			{% if intervention.slides %}
			  <a href="{{ intervention.slides }}" class="intervention-link">[Slides]</a>
			{% endif %}
			{% if intervention.paper %}
			  <a href="{{ intervention.paper }}" class="intervention-link">[Paper]</a>
			{% endif %}
			{% if intervention.video %}
			  <a href="{{ intervention.video }}" class="intervention-link">[Video]</a>
			{% endif %}
		  </h2>
		</div>
      {% if intervention.presenter %}
		<div class="intervention-presenter presenter-info">
		  <img src="{{ intervention.presenter.image  | relative_url }}" alt="{{ intervention.presenter.name }}" class="circular-image">
		  <div class="presenter-info-container">
			Presenter: 
			<a href="{{ intervention.presenter.url }}">{{ intervention.presenter.name }}</a>
			{% if intervention.presenter.affiliation %}
			  <div>
				{{ intervention.presenter.affiliation }}
			  </div>
			{% endif %}
		  </div>
		</div>      {% endif %}
	  <h3> Abstract: </h3>
      <div class="intervention-abstract">{{ intervention.abstract | markdownify  }}</div>
    </div>
	   <hr />
	{% endfor %}
</div>

