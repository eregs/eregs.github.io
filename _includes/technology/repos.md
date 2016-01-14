## Repositories

There are many individual repositories that make up eRegulations; this is
complicated by having two primary forks maintained by CFPB and 18F
respectively. While these forks will ultimately be merged and maintenance
shared between multiple agencies, those interested in using eRegs now should
generally prefer the 18F repositories.

{% if site.general_repos %}
<section id="main-repositories">
  <h3 id="repositories">General Purpose</h3>
  {% include technology/repo_sublist.html repos=site.general_repos %}
</section>
{% endif %}

{% if site.agency_repos %}
<section id="agency-repositories">
  <h3 id="repositories">Agency-Specific Repos</h3>
  {% for agency in site.agency_repos %}
    <h4>{{agency.name}}</h4>
    {% include technology/repo_sublist.html repos=agency.repos %}
  {% endfor %}
</section>
{% endif %}
