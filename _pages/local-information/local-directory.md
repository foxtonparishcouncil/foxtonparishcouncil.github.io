---
title: "Local Directory"
permalink: /local-information/local-directory
historic_url: http://foxtonparishcouncil.gov.uk/directory.php?id=22
layout: simple
sidebar:
  nav: local-info
---

You can use the Local Directory to find details of local organisations in the local area. If you would like to add an entry into one of the categories below, or if you wish to update your details, please contact us. You can search by category, or just type the name of what you are looking for into the box below:

<!--
The previous website had a search box which did appear to work but wasn't really needed?
<select name="select" size="1" >
 <option value="#" selected="">[ select a category to display ]</option>
 <option value="Churches">Churches</option>
 <option value="Fundraising Groups&amp">Fundraising Groups</option>
 <option value="Health">Health</option>
 <option value="Local publications">Local publications</option>
 <option value="Other Groups">Other Groups</option>
 <option value="Schools and Playgroups">Schools and Playgroups</option>
 <option value="Sports Groups">Sports Groups</option>
 <option value="Village Amenities">Village Amenities</option>
</select>
There was all a button to show all the entries
-->

{% assign collection = site.directory | sort: 'title' %}
 {% unless collection.output == false or collection.label == "posts" %}

 {% for entry in collection %}
<div>
   <strong><a href="{{ entry.url}}">{{ entry.title }}</a></strong>
   {% if entry.categories %}
   <small>({{ entry.categories | array_to_sentence_string }})</small>
   {% endif %}
  
  <!---->
   <br>

   {% if entry.contact_name %} <i class="fas fa-user-circle"></i> {{ entry.contact_name }}<br>{% endif %}
   {% if entry.contact_name %} <i class="fas fa-envelope"></i> {{ entry.email }}<br>{% endif %}
   {% if entry.telephone_number %} <i class="fas fa-phone fa-rotate-90"></i> {{ entry.telephone_number }}<br>{% endif %}
   {% if entry.website %} <i class="fas fa-link"></i> {{ entry.website }}<br>{% endif %}
  <!---->
   
</div>
<hr>
 {% endfor %}
 {% endunless %}


