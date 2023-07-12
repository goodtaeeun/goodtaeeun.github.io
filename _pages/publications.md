---
# layout: splash
permalink: /publications/
classes: wide
author_profile: true
---

<!-- ## Publications -->
{% assign year_printed = 0 %}
{% assign list_opened = false %}

{% for pub in site.data.publications %}
{% if year_printed != pub.year %}
{% if list_opened == true %}
</ul>
{% endif %}
<h3> {{ pub.year }} </h3>
<ul>
{% assign list_opened = true %}
{% assign year_printed = pub.year %}
{% endif %}
<li>{{pub.title}}<br>
{% for author in pub.author %}
{% if forloop.last %}
and {{ author }}
{% else %}
{{ author }},
{% endif %}
{% endfor %}
  {% if pub.award != nil %}
    <br>&#127942; <b>{{pub.award}}</b>
  {% endif %}
  {% if pub.misc != nil %}
  <br><b>{{ pub.misc }}</b>
  {% endif %}
  <br>
  <a href="{{ pub.venue_link }}">{{ pub.venue }}</a>, {{ pub.year }}
   <br>
  {% if pub.paper != nil %}
  [<a href="{{ site.baseurl }}/{{ pub.paper }}">paper</a>]
  {% endif %}
  {% if pub.full != nil %}
    [<a href="{{ site.baseurl }}/{{ pub.full }}">full-version</a>]
  {% endif %}
  {% if pub.slides != nil %}
    [<a href="{{ site.baseurl }}/{{ pub.slides }}">slides</a>]
  {% endif %}
  {% if pub.video != nil %}
    <a href="{{ pub.video }}"><i class="fab fa-youtube" style="font-size: 20px; vertical-align: middle"></i></a>
  {% endif %}
  {% if pub.code != nil %}
    <a href="{{ pub.code }}"><i class="fab fa-github" style="font-size: 20px; vertical-align: middle"></i></a>
  {% endif %}
  {% if pub.project_page != nil %}
    <a href="{{ pub.project_page }}"><i class="fas fa-home" style="font-size: 20px; vertical-align: middle"></i></a>
  {% endif %}
  </li>
{% endfor %}
