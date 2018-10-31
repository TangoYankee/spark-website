---
title: Policies
permalink: /policies/
layout: page
sidenav: policies
---
<!-- Section names and addresses from navigation bar -->
{% assign nav_data = site.data.navigation.policies %}

<!-- policies-->
{% assign policies_data = site.data.policies %}

<!-- Iterate through all of the navigation sections. -->
{% for section in nav_data %}
<a name="{{ section.text | slugify }}"></a>
<h2>{{ section.text }}</h2>
<hr>

<!-- In each section, get only the policies assigned to it -->
{% assign section_data = policies_data | where:"section",section.text %}

<!-- Display the information for all of the policies assigned to that section -->
{% for each_policies in section_data %}
<div>
 <h3>{{ each_policies.title }}</h3>
 <p>{{ each_policies.desc }}</p>
</div>

<!-- Close policies Iteration -->
{% endfor %}

<!-- Close Section Iteration -->
{% endfor %}