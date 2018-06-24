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
<form action="https://docs.google.com/forms/d/e/1FAIpQLSdTDqh0WWT3WccMbaW_C2hW6fR-QKex5qTx3f30CIOcXieeKA/formResponse">
    <a name="personal-information"></a>
    <h2>Personal Information</h2>
    <!--  -->
    <label for="personal-name">Name</label>
    <input id="personal-name" name="entry.2005620554" required>
    <!--  -->
    <label for="personal-email">Email</label>
    <input id="personal-email" name="entry.1045781291" required>
    <!--  -->
    <a name="organization-information"></a>
    <h2>Organization Information</h2>
    <!--  -->
    <label for="organization-name">Organization Name</label>
    <input id="organization-name" name="entry.1166974658">
    <!--  -->
    <label for="organization-type">Type of Organization</label>
    <select name="entry.1875847283" id="organization-type">
        <option value>-Select-</option>
        <option value="Department of Defense">Department of Defense</option>
        <option value="Government (Non DoD)">Government (Non DoD)</option>
        <option value="Academia">Academia</option>
        <option value="Non-Profit">Non-Profit</option>
        <option value="Commercial Industry">Commercial Industry</option>
        <option value="Other">Other</option>
    </select>
    <!--  -->
    <a name="interest-areas"></a>
    <h2>Areas of Interest</h2>
    <!--  -->
    <fieldset class="usa-fieldset-inputs usa-sans">
        <label for="interest-areas">Topics</label>
        <legend class="usa-sr-only">Interest Areas</legend>
        <ul class="usa-unstyled-list">
            <li>
                <input id="os-soft" type="checkbox" name="entry.521051122" value="Open Source Software">
                <label for="os-soft">Open Source Software</label>
            </li>
            <li>
                <input id="mach-learn" type="checkbox" name="entry.521051122" value="Machine Learning">
                <label for="mach-learn">Machine Learning</label>
            </li>
            <li>
                <input id="virt-real" type="checkbox" name="entry.521051122" value="Virtual Reality">
                <label for="virt-real">Virtual Reality</label>
            </li>
            <li>
                <input id="robots" type="checkbox" name="entry.521051122" value="Automation & Robotics">
                <label for="robots">Automation & Robotics</label>
            </li>
            <li>
                <input id="printing" type="checkbox" name="entry.521051122" value="3D-Printing">
                <label for="printing">3D-Printing</label>
            </li>
            <li>
                <input id="manufact" type="checkbox" name="entry.521051122" value="Manufacturing">
                <label for="manufact">Manufacturing</label>
            </li>
            <li>
                <input id="op-manange" type="checkbox" name="entry.521051122" value="Operational Management Theory">
                <label for="op-manange">Operational Management Theory</label>
            </li>
        </ul>
    </fieldset>
    <!--  -->
    <label for="message">Message</label>
    <textarea id="message" name="entry.839337160"></textarea>
    <!--  -->
    <p>This service is provided by <a href="https://docs.google.com/forms">Google Forms</a></p>
    <input type="submit" value="Submit">
</form>