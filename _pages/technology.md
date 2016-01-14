---
layout: default
title: Technology
subtemplates: [architecture, stack, repos]
---
# Technology

{% for subtemplate in page.subtemplates %}
  {% capture subtemplate_file %}technology/{{subtemplate}}.md{% endcapture %}
  {% capture markdown %}{% include {{subtemplate_file}} %}{% endcapture %}
  {{ markdown | markdownify }}
{% endfor %}

