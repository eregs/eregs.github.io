
## Repositories

There are many individual repositories that make up eRegulations. These are divided below into the main body of eRegulations, tools to support eRegulations, and finally CFPB-specific modifications and data for eRegulations.

{% if site.repos %}
<section id="main-repositories">
  <h3 id="repositories">eRegulations</h3>
  <ul class="repo-list group">
    <li class="list-icon">
      <img src="assets/img/octocat.png" width="25px" alt="">
    </li>
    {% for repo in site.repos %}
      <li>
        <a href="{{ repo.url }}">
          <h4>{{ repo.name }}</h4>
          <p>{{ repo.description }}</p>
        </a>
      </li>
    {% endfor %}
  </ul>
</section>
{% endif %}

{% if site.support_repos %}
<section id="support-repositories">
  <h3 id="repositories">Support</h3>
  <ul class="repo-list group">
    <li class="list-icon">
      <img src="assets/img/octocat.png" width="25px" alt="">
    </li>
    {% for repo in site.support_repos %}
      <li>
        <a href="{{ repo.url }}">
          <h4>{{ repo.name }}</h4>
          <p>{{ repo.description }}</p>
        </a>
      </li>
    {% endfor %}
  </ul>
</section>
{% endif %}

{% if site.cfpb_repos %}
<section id="cfpb-repositories">
  <h3 id="repositories">CFPB-Specific</h3>
  <ul class="repo-list group">
    <li class="list-icon">
      <img src="assets/img/octocat.png" width="25px" alt="">
    </li>
    {% for repo in site.cfpb_repos %}
      <li>
        <a href="{{ repo.url }}">
          <h4>{{ repo.name }}</h4>
          <p>{{ repo.description }}</p>
        </a>
      </li>
    {% endfor %}
  </ul>
</section>
{% endif %}

