---
layout: default
title: Creating an eRegulations instance
---

# Creating an eRegulations instance

## Building with the platform

If you develop features or improvements that would benefit other agencies who use eRegulations, it makes sense to contribute them to the core cross-agency shared code libraries, which are [**regulations-core**](https://github.com/eregs/regulations-core), [**regulations-site**](https://github.com/eregs/regulations-site), and [**regulations-parser**](https://github.com/eregs/regulations-parser). We don't have a very good "raw" eRegulations right now, though we're slowly moving there. "Raw" eRegulations is basically CFPB eRegulations right now.

At this point, you would probably never run **regulations-site** or **regulations-core** on their own. Instead, they're libraries, and you can modify them as libraries. Effectively, you point a wrapper to local checkouts. For an example of a wrapper, see [**atf-eregs**](https://github.com/18F/atf-eregs).

Adding agency-specific styles, markup, and even certain types of features (specific to those agencies) should not require modifications to the core repositories. Instead, those can go in the agency-specific wrapper.

### Share or fork the codebase? Specific features or generalizable features?

Each reuse of eRegulations faces a tradeoff: fork the codebase, or make the effort to work to share the main codebase? Build features specific to the agency, or try to build more generically reusable features even if it takes more time? It's important to plan to use the shared codebase and to build features that are relatively reusable—and to balance this vision with the pragmatic needs of your budget.

The work to make it generalizable is good for each agency. Each agency benefits from the generalizing work of previous agencies, and all clients will themselves benefit when, inevitably, they produce regulations in the future with quirks that will be easier to handle within an extensible/generalizable system.

We are not sure how long-term cross-agency maintenance will work yet. We'll figure it out together.

## Theming an instance

If you’re building an instance of eRegulations for a specific agency, you’ll probably want to customize the templates and styles to fit the agency’s needs.

The [**regulations-site**](https://github.com/eregs/regulations-site) repository contains a base theme that provides a relatively neutral-looking default user interface. This is implemented by a set of [Django templates](https://docs.djangoproject.com/en/1.9/topics/templates/#the-django-template-language) styled using the [Sass](http://sass-lang.com/) stylesheet language. All of this is designed so that you can build "overriding" files in an agency-specific wrapper repository, instead of directly modifying the base files in **regulations-site**.

For the big picture, see [this explanation of customizing ATF eRegulations](https://atf-eregs.readthedocs.org/en/latest/customization.html).

## Customize the styles

For context on how **regulations-site** works, check out [that readme](https://github.com/eregs/regulations-site). Then, you can start customizing it.

### System-wide styles

The `compile_frontend` command (i.e. `python manage.py compile_frontend`) uses a variant of Django's `collectstatic` to combine static assets between the base application (**regulations-site**) and any custom Django application you develop. It is designed as a simple file **override** scheme — create an identically named file in your `static/regulations/` directory and it will replace the file in the base application. In this way, you can modify stylesheets, images, etc. when building the front end.

The `compile_frontend` command generates output indicating which files are being overridden.

#### Django templates tip

You might find [django-overextends](https://github.com/stephenmcd/django-overextends) helpful; see [this usage in ATF eRegulations for an example](https://github.com/18F/atf-eregs/blob/master/atf_eregs/templates/regulations/generic_landing.html#L1).

### Individual paragraphs

The templates used to generate paragraphs can be replaced selectively, which is useful if you want to emphasize a particular paragraph or add links to external sources that don’t exist in the regulation itself. Note that this mechanism is intended for one-offs; consider modifying the data structures instead if you find yourself using it often.

To use this override mechanism, create a `templates/regulations/custom_nodes` directory in your Django application if it doesn't already exist. Inside that folder, create files corresponding to node labels, such as, `478-103-b.html`. These templates will be used **in place** of the `tree-with-wrapper.html` template, so be sure to provide the functionality already present there. Should you need to use this functionality only on specific versions, your template can make use of the `version` context variable.

## Customize the stylesheets

The base theme is designed to be customized with [Sass](http://sass-lang.com/) variables (`_variables.scss`) and mixins (`_custom.scss`), particularly font mixins.
You can build "overriding" files in an agency-specific wrapper repository, instead of directly modifying the base files in **regulations-site**. For an example (using Less), see [these .less files in **atf-eregs**](https://github.com/18F/atf-eregs/tree/master/atf_eregs/static/regulations/css/less).

### Font mixins

You can do most font theming by including the basic font mixins to create specific formatting rules for different types of content. Here’s an example that declares a basic font and then creates a variation with a particular size and line height for a specific type of content within the theme:

``` scss
@mixin sans-font-regular {
  font-family: "Source Sans Pro", Arial, sans-serif;
  font-weight: 400;
  font-style: normal;
}
@mixin regulation-nav-item-font {
  @include sans-font-regular;
  font-size: 1em;
  line-height: 20px;
}
```

This approach allows for variation in typography without needing to create a lot of customization variables (`$regulation_nav_item_font_size`, etc) for one-off styling choices.

### Agency specific stylesheets

Overriding base files in **regulations-site** is simple. In the agency-specific repo, list overriding custom stylesheets in (`/css/scss/module/_custom.scss`):

``` sass
// custom imports
@import '../comment-custom';
@import '../layout-custom';
// Custom Modules
@import 'header-custom';
@import 'note-custom';
```

Additional variables will similarly reside in `/css/scss/_variables.scss`.
