---
layout: page
title: Training
permalink: /training/
---

Training list coming soon.



# Upcoming Meetings

<table>

{% for training in site.data.training %}
{% capture day %}{{meeting.day}}{% endcapture %}
{% endif %}
{% capture event_date_string %} {{ meeting.year }}-{{ meeting.month }}-{{day}} {% endcapture %}
{% capture event_date %}{{ event_date_string | date: '%s' }}{% endcapture %}
{% capture current_date %}{{ site.time | date: '%s' }}{% endcapture %}
{% if event_date >= current_date %}
<tr>
<td bgcolor="#D3D3D3" colspan="3">{{ training.title }}</td>
<tr>
<td colspan="3">{{ training.subtitle}}</td>
</tr>
<tr>
<td colspan="3">{{ training.description}}</td>
</tr>
<tr bgcolor="#D3D3D3">
<td>{{ training.day }} {{ training.month }} {{ training.year }}</td>
<td>{{ training.institute }}</td>
</tr>
{% endif %}
{% endfor %}
</table>
