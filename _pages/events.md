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
{% assign events_data = site.data.events | sort:"date" %}

<!-- Find length of Navigation Array, iterate through this later -->
{% assign end_nav_data = nav_data | size | minus:1 %}

<!-- Iterate through all of the navigation sections. Start at one because zero is just the top header -->
{% for section_count in (1..end_nav_data ) %}
<a name="{{ nav_data[section_count].text | slugify }}"></a>
<h2>{{ nav_data[section_count].text }}</h2>
<hr>

<!-- In each section, get only the events assigned to it -->
{% assign section_data = events_data | where:"section",nav_data[section_count].text %}

<!-- Display the information for all of the events assigned to that section -->
{% for each_event in section_data %}
 <section>{{ each_event.title }}</section>

<!-- Close events Article Iteration -->
{% endfor %}

<!-- Close Section Iteration -->
{% endfor %}