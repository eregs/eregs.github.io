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

[CFPB released its initial version of eRegulations in 2013](http://www.consumerfinance.gov/blog/making-regulations-easier-to-use/), and [18F and ATF began reusing it for ATF in 2015](https://18f.gsa.gov/2015/12/09/an-open-source-government-is-a-faster-more-efficient-government/). We would like other agencies, developers, and groups to use it and adapt it as well.