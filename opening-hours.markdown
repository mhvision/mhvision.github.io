---
title: Opening Hours
date: 2016-10-30 09:47:00 +01:00
---

{% assign foo = site.time | date: "%A" | downcase %}

{{ site.openingHours.days\[foo\] }}

<script src="https://cdnjs.cloudflare.com/ajax/libs/jquery/3.1.1/jquery.min.js" ></script>

<script src="https://cdnjs.cloudflare.com/ajax/libs/moment.js/2.15.2/moment.min.js"></script>

<script>
var openingHours = {{ site.openingHours | jsonify }};
</script>

<ul>
{% for day in site.openingHours.days %}
<li>\
{{ day\[1\].name }}\
{% if day\[1\].timeRange or day\[1\].timeRanges %}\
{% else %}

* Fermé\
  {% endif %}

{% if day\[1\].comment %}
<p>{{ day\[1\].comment }}</p>\
{% endif %}

<ul>
{% if day\[1\].time-range %}
{% for hour in site.openingHours.timeRange.classic %}
<li>{{ hour.from }}-{{ hour.to }}</li>\
{% endfor %}
{% endif %}

{% if day\[1\].timeRanges  %}\
{% for hour in day\[1\].timeRanges %}
<li>{{ hour.from }}-{{ hour.to }}</li>
{% endfor %}
{% endif %}
</ul>
</li>
{% endfor %}
</ul>