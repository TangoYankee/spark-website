---
title: Events
permalink: /events/

layout: page
sidenav: events

# subnav:
#   - text: Section one
#     href: '#section-one'
#   - text: Section two
#     href: '#section-two'
---
<!-- Section names and addresses from navigation bar -->
{% assign nav_data = site.data.navigation.events %}

<!-- events Sorted by First to occur-->
{% assign events_data = site.data.events | sort:"start_date" %}

<!-- Iterate through all of the navigation sections.-->
{% for section in nav_data %}

<a name="{{ section.text | slugify }}"></a>
<h2>{{ section.text }}</h2>
<hr>

<!-- In each section, get only the events assigned to it -->
{% assign section_data = events_data | where:"section",section.text %}

<!-- Display the information for all of the events assigned to that section -->
{% for each_event in section_data %}
<div>
 <h3>{{ each_event.title }}</h3>
 <p><i>{{ each_event.location }}<br>{{ each_event.text_date }}</i></p>
 <p>{{ each_event.desc }}</p>
 <a href="{{ each_event.event_url }}">More Information</a>
 </div>

<!-- Close events Article Iteration -->
{% endfor %}

<!-- Close Section Iteration -->
{% endfor %}
