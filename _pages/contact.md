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

<!-- Find length of Navigation Array, iterate through this later (Legacy Feature) -->
<!-- {% assign end_nav_data = nav_data | size | minus:1 %} -->

<!-- Iterate through all of the navigation sections. Start at one because zero is just the top header (Legacy Feature) -->
{% for section_count in (0..nav_data ) %}
<a name="{{ nav_data[section_count].text | slugify }}"></a>
<h2>{{ nav_data[section_count].text }}</h2>
<hr>

<!-- In each section, get only the policies assigned to it -->
{% assign section_data = policies_data | where:"section",nav_data[section_count].text %}

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