---
layout: default
title: Technology
subtemplates: [architecture, stack, repos]
---
# Code and repositories

## How eRegulations works

{% for subtemplate in page.subtemplates %}
  {% capture subtemplate_file %}technology/{{subtemplate}}.md{% endcapture %}
  {% capture markdown %}{% include {{subtemplate_file}} %}{% endcapture %}
  {{ markdown | markdownify }}
{% endfor %}


## Open source and contributing

We invite [contributions](/contributing/) to any part of the application, from people inside and outside government. The project is in the [public domain](/contributing/#public-domain), and all contributions to it will be released as such.
