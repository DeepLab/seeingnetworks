---
layout: cities
title: New York City
city: nyc
intro: "New York's network infrastructure is a lot like the city itself: messy, sprawling, and at times near-incomprehensible. However, the city's tendency toward flux is a strange blessing for the infrastructure sightseer: markings and remnants of the network are almost everywhere, once you know how to look for them."
---

<div id="content">
  {% for category in site.data.nyc-meta %}
    <div class="jumbotron section" id="{{category.category}}">
    <h1>{{category.title}}</h1>
    <span id="mark"><p>{{category.summary}}</p></span>
    </div>
      <div class="container-fluid">
     {% for data in site.data.nyc %}
     {% if data.category == category.category %}
       {% if data.img != null %}
        <div class="row">
          <div class="col-md-3 object"><img src="{{data.img}}" class="img-responsive"></div>
          <div class="col-md-8">
            <h2>{{data.name}}</h2>
            <p>{{data.desc}}</p>
          </div>
        </div>
      {% else %}
        <div class="row">
          <div class="col-md-12">
            <h2>{{data.name}}</h2>
            <p>{{data.desc}}</p>
          </div>
        </div>
    {% endif %}
    {% endif %}
    {% endfor %}
  </div>
  {% endfor %}
</div>
