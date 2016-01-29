## Live instances

The application is typically hosted by individual federal agencies, with
features and branding unique to their users and needs. Current instances of
eRegs include:

<section>
  <ul class="group">
    {% for instance in site.instances %}
      <li>
        <a href="{{ instance.url }}">
          <h4>CFR {{ instance.title }}</h4>
          <p>{{ instance.agency }}</p>
        </a>
      </li>
    {% endfor %}
  </ul>
</section>
