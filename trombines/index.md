---
layout: page
title:
excerpt: "Les Bricodeurs, c'est comme à la maison"
modified: 2015-07-24T19:44:38.564948-04:00
image:
  feature:
  credit:
  creditlink:
---


{% for member_data in site.data.members %}
{% assign member = member_data[1]  %}
  <div class="bio">
  	<img alt="{{ member.name }}" src="{{ site.url }}/images/{{ member.avatar }}" class="bio-photo">
  	<h4> {{member.name}}</h4>
  	<i>{{member.bio}}</i>
    <div>
      {% if member.twitter%}
      <a class="twitter-link" href="http://twitter.com/{{ member.twitter }}" title="{{ member.name }} on Twitter" target="_blank">
        <i class="fa fa-twitter-square fa-2x"></i>
      </a>
      {% endif %}
      {% if member.email%}
      <a class="email-link" href="mailto:{{ member.email }}" title="Email to {{ member.name }}" target="_blank">
        <i class="fa fa-envelope-square fa-2x"></i>
      </a>
      {% endif %}
      {% if member.web%}
      <a class="web-link" href="{{ member.web }}" title="{{ member.name }}'s website" target="_blank">
        <i class="fa fa-external-link-square fa-2x"></i>
      </a>
      {% endif %}


    </div>

  </div>
{% endfor %}
