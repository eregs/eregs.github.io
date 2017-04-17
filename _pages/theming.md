---
layout: default
title: Theming an instance
---

# Theming an instance

If you’re building an adaptation of eRegulations (such as for a specific agency), you’ll probably want to customize that instance to fit the agency’s needs. Here's how to customize the templates, styles, and supporting content.

**Table of contents**

* [Overview](#overview)
* [How to customize the frontend in general](#how-to-customize-the-frontend-in-general)
* [How to customize the Sass stylesheets](#how-to-customize-the-sass-stylesheets)
* [Agency specific stylesheets](#agency-specific-stylesheets)

## Overview

The [**regulations-site**](https://github.com/eregs/regulations-site) repository contains a base theme that provides a relatively neutral-looking default eRegulations user interface. This is implemented by a set of [Django templates](https://docs.djangoproject.com/en/1.9/topics/templates/#the-django-template-language) styled using the [Sass](http://sass-lang.com/) stylesheet language.

All of this is designed so that you can build "overriding" files in an agency-specific wrapper repository, instead of directly modifying the base files in **regulations-site**.

For the big picture, see [this explanation of customizing ATF eRegulations](https://atf-eregs.readthedocs.org/en/latest/customization.html).

## How to customize the frontend

For context on how **regulations-site** works, check out [that readme](https://github.com/eregs/regulations-site). Then here's how to start customizing it.

### System-wide styles

The `compile_frontend` command (i.e. `python manage.py compile_frontend`)
uses a variant of Django's `collectstatic` to combine static assets between
the base application (regulations-site) and any custom Django application you
develop. It is designed as a simple file **override** scheme — create an
identically named file in your `static/regulations/` directory and it will
replace the file in the base application. In this way, you can modify
stylesheets, images, etc. when building the frontend.

The `compile_frontend` command generates output indicating which files are
being overridden.

### Individual paragraphs

The templates used to generate paragraphs can be replaced selectively, a
useful technique if you want to emphasize a particular paragraph or add links
to external sources that don't exist in the regulation proper. Note that this
mechanism is intended for one-offs; consider the method of modifying the data
structures instead if you find yourself using it often.

To use this override mechanism, create a `templates/regulations/custom_nodes`
directory in your Django application if it doesn't already exist. Inside that
folder, create files corresponding to node labels, e.g. `478-103-b.html`.
These templates will be used **in place** of the `tree-with-wrapper.html`
template, so be sure to provide the functionality already present there.
Should you need to use this functionality only on specific versions, your
template can make use of the `version` context variable.

### Django templates tip

You might find [django-overextends](https://github.com/stephenmcd/django-overextends) helpful; see [this usage in ATF eRegulations for an example](https://github.com/18F/atf-eregs/blob/master/atf_eregs/templates/regulations/generic_landing.html#L1).

## How to customize the Sass stylesheets

This section explains eRegulations theming from the Sass/CSS perspective.

The base theme is heavily parameterized to allow for customization. It’s designed to be customized through the use of sass variables (`_variables.scss`) and mixins (`_custom.scss`), particularly font mixins.

This is designed so that you can build "overriding" files in an agency-specific wrapper repository, instead of directly modifying the base files in **regulations-site**. For an example (but using Less), see [these .less files in **atf-eregs**](https://github.com/18F/atf-eregs/tree/master/atf_eregs/static/regulations/css/less).

### Font mixins

You can do most font theming by including the basic font mixins to create specific formatting rules for different types of content. Here’s an example that declares a basic font and then creates a variation with a particular size and line height to use for a specific type of content within the theme:

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

This approach allows for a lot of variation in typography without needing to create a lot of customization variables (i.e. `$regulation_nav_item_font_size`, etc) for one-off styling choices.

## Agency specific stylesheets

Overriding base files in **regulations-site** is very simple. In the agency-specific repo, list overriding custom stylesheets in (`/css/scss/module/_custom.scss`):

``` sass
// custom imports
@import '../comment-custom';
@import '../layout-custom';

// Custom Modules
@import 'header-custom';
@import 'note-custom';
```

Additional variables will similarly reside in (`/css/scss/_variables.scss`)
