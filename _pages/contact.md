---
title: Contact Us
permalink: /contact/

layout: page
sidenav: contact

# subnav:
#   - text: Section one
#     href: '#section-one'
#   - text: Section two
#     href: '#section-two'
---
{% assign contact_data = site.data.contact %}
{% assign nav_data = site.data.navigation.contact %}

<form action="{{ contact_data.google-forms.action-link}}">
    <!-- Section: Personal Information -->
    <a name="{{ nav_data[0].text | slugify }}"></a>
    <h2>{{ nav_data[0].text }}</h2>
    <!-- Input: User Name -->
    <label for="{{ contact_data.personal-name.id }}">{{ site.data.contact.personal-name.text }}</label>
    <input id="{{ contact_data.personal-name.id }}" name="{{contact_data.personal-name.name}}" required>
    <!-- Input: User Email -->
    <label for="{{ contact_data.personal-email.id }}">{{ contact_data.personal-email.text }}</label>
    <input id="{{ contact_data.personal-email.id }}" name="{{ contact_data.personal-email.name }}" required>
    <!-- Section: Organization Information -->
    <a name="{{ nav_data[1].text | slugify}}"></a>
    <h2>{{ nav_data[1].text }}</h2>
    <!-- Input: Organization Name -->
    <label for="{{ contact_data.organization-name.id }}">{{ contact_data.organization-name.text }}</label>
    <input id="{{ contact_data.organization-name.id }}" name="{{ contact_data.organization-name.name }}">
    <!-- Input: Type of Organization -->
    <label for="{{ contact_data.organization-type.id }}">{{ contact_data.organization-type.text }}</label>
    <select name="{{ contact_data.organization-type.name }}" id="{{ contact_data.organization-type.id }}">
        <option value>-Select-</option>
        <!-- Selection: Cycle through Types of Organizations-->
        {% for each_type in contact_data.organization-type.types %}
            <option value="{{ each_type }}">{{ each_type }}</option>
        {% endfor %}
        <!--  -->
    </select>
    <!-- Section: Areas of Interest -->
    <a name="{{ nav_data[2].text | slugify }}"></a>
    <h2>{{ nav_data[2].text }}</h2>
    <!-- Input: Areas of Interest -->
    <fieldset class="usa-fieldset-inputs usa-sans">
        <label for="{{ contact_data.interest-areas.id }}">{{ contact_data.interest-areas.text }}</label>
        <legend class="usa-sr-only">{{ contact_data.interest-areas.legend }}</legend>
        <ul class="usa-unstyled-list">
        <!-- CheckBox that cycles through all interest areas -->
        {% for each_area in contact_data.interest-areas.areas %}
            <li>
                <input id="{{ each_area | slugify }}" type="checkbox" name="{{ contact_data.interest-areas.name }}" value="{{ each_area }}">
                <label for="{{ each_area | slugify }}">{{ each_area }}</label>
            </li>
        {% endfor %}
        </ul>
    </fieldset>
    <!-- Input: 26 Oct Programming event -->
    <!-- <fieldset class="usa-fieldset-inputs usa-sans">
        <label for="{{ contact_data.event-interest.id }}">{{ contact_data.event-interest.legend }}</label>
        <legend class="usa-sr-only">{{ contact_data.event-interest.legend }}</legend>
            <input id ="{{ contact_data.event-interest.value | slugify }}" type="checkbox" name="{{ contact_data.event-interest.name }}" value="{{ contact_data.event-interest.value }}">
            <label for="{{ contact_data.event-interest.value | slugify }}">{{ contact_data.event-interest.text }}</label>
    </fieldset> -->
    <!-- Input: User Message -->
    <label for="{{ contact_data.user-message.id }}">{{ contact_data.user-message.text }}</label>
    <textarea id="{{ contact_data.user-message.id }}" name="{{ contact_data.user-message.name }}"></textarea>
    <!-- Google Forms Information -->
    <p> {{ contact_data.google-forms.message }}<a href="{{ contact_data.google-forms.home-link }}">{{ contact_data.google-forms.text }}</a><br><i>{{ contact_data.google-forms.disclaimer }}</i></p>
    <input type="submit" value="Submit">
</form>
