## Repositories

There are many individual repositories that make up eRegulations. The project is divided into several components, and currently CFPB and 18F maintain two separate forks of **regulations-parser**, **regulations-core**, and **regulations-site**. 18F and CFPB plan to eventually merge these forks into shared components with maintenance shared between multiple agencies. For now, in most cases people interested in using eRegulations should use the 18F repositories.

*Tip: If you'd like to get an example eRegulations site set up to try it out, check out [CFPB **regulations-bootstrap**](https://github.com/cfpb/regulations-bootstrap) to install a CFPB-centric version.*

{% if site.general_repos %}
<section id="main-repositories">
  <h3 id="repositories">The main body of eRegulations (not agency-specific)</h3>
  {% include technology/repo_sublist.html repos=site.general_repos %}
</section>
{% endif %}

{% if site.agency_repos %}
<section id="agency-repositories">
  <h3 id="repositories">Agency-centric components</h3>  
  {% for agency in site.agency_repos %}
    <h4>{{agency.name}}</h4>
    {% include technology/repo_sublist.html repos=agency.repos %}
  {% endfor %}
</section>
{% endif %}
