---
layout: archive
permalink: /application-development/ 
title: "Application Development Posts by Tags"
author_profile: true
header:
    image: "/images/jslogo.png"
---
{% include base_path %}
{% include group-by-array collection=site.posts field="tags" %}

{% for tag in group_names %}
    {% assign posts = group_items[forloop.index0] %}
    <h2> id="{{ tag | uglify }}" class="archive_subtitle">{{ tag }}</h2>
    {% for post in posts %}
        {% include archive-single.html %}
    {% endfor %}
{% endfor %}