---
layout: default
title: Theming an instance
---

# Theming an instance

**Table of contents**

* [How to theme an eRegulations site](#how-to-theme-an-eregulations-site)
* [Potential ways to improve the theming layer](#potential-ways-to-improve-the-theming-layer)

# How to theme an eRegulations instance

## Overview

The [**regulations-site**](https://github.com/18F/regulations-site) repository contains a base theme that provides a relatively neutral-looking default eRegulations user interface. This is implemented by a set of [Django templates](https://docs.djangoproject.com/en/1.9/topics/templates/#the-django-template-language) styled using the [Less](http://lesscss.org/) stylesheet language.

If you’re building an adaptation of eRegulations (such as for a specific agency), you’ll probably want to customize that theme to fit the agency’s needs. This page explains eRegulations theming from the Less/CSS perspective.

The base theme is heavily parameterized to allow for customization. It’s designed to be customized through the use of less variables (`variables.less`) and less mixins (`custom.less`), particularly font mixins.

This is designed so that you can build "overriding" files in an agency-specific wrapper repository, instead of directly modifying the base files in **regulations-site**. For example, see [these .less files in **atf-eregs**](https://github.com/18F/atf-eregs/tree/master/atf_eregs/static/regulations/css/less).

See also: [this explanation of customization for ATF eRegulations](https://atf-eregs.readthedocs.org/en/latest/customization.html).

### Font mixins

You can do most font theming by `extend`ing the basic font mixins to create specific formatting rules for different types of content. Here’s an example that declares a basic font and then creates a variation with a particular size and line height to use for a specific type of content within the theme:

``` less
.font-regular {
  font-family: 'Lato Regular', Arial, sans-serif;
}

/* Regulation nav (drawer) font styles */
.regulation-nav-item-font {
    &:extend(.font-regular);
    font-size: 1em;
    line-height: 20px;
}
```

That example produces this CSS:

``` css
.font-regular,
.regulation-nav-item-font {
  font-family: 'Lato Regular', Arial, sans-serif;
}
/* Regulation nav (drawer) font styles */
.regulation-nav-item-font {
  font-size: 1em;
  line-height: 20px;
}
```

This approach allows for a lot of variation in typography without needing to create a lot of customization variables (i.e. `@regulation_nav_item_font_size`, etc) for one-off styling choices.

### Less `&:extend(.foo)` compared to `.foo`

Less mixins can reference other mixins in two ways: by either *extending* them or *including* them. These options are largely the same, but there are some differences. For example, you can replace `&:extend(.font-regular)` with `.font-regular` in the previous example, like this:

``` less
font-regular {
  font-family: 'Lato Regular', Arial, sans-serif;
}

/* Regulation nav (drawer) font styles */
.regulation-nav-item-font {
    .font-regular;
    font-size: 1em;
    line-height: 20px;
}
```

That new example produces this CSS:

``` css
.font-regular {
  font-family: 'Lato Regular', Arial, sans-serif;
}
/* Regulation nav (drawer) font styles */
.regulation-nav-item-font {
  font-family: 'Lato Regular', Arial, sans-serif;
  font-size: 1em;
  line-height: 20px;
}
```

The two options produce CSS with different structures — the earlier example is a little more compact. One important difference is that `.foo` will simply copy the `.foo` style attributes in place. This means that order does matter. Any attributes before the included mixin will get overridden by the same values in the mixin, such as `font-size` in the following example:

``` less
.font-regular {
  font-family: 'Lato Regular', Arial, sans-serif;
  font-size:1em;
}

/* Regulation nav (drawer) font styles */

.regulation-nav-item-font {
  font-size: 2em;
  .font-regular;
  line-height: 20px;
}
```

That example produces this CSS:

``` css
.font-regular {
  font-family: 'Lato Regular', Arial, sans-serif;
  font-size: 1em;
}

/* Regulation nav (drawer) font styles */
.regulation-nav-item-font {
  font-size: 2em;
  font-family: 'Lato Regular', Arial, sans-serif;
  font-size: 1em;
  line-height: 20px;
}
```

With `extend`, the resulting font-size would be different as the extended attributes are grouped at a higher level.

# Potential ways to improve the theming layer

Theming eRegulations is a work in progress! Here are a few ways that contributors could make it better.

## Start with a generalized theme

The current theming efforts have taken the approach of trying to create a general theme based on specific implementations (CFPB / ATF). A lot could be gained by looking at regulations and identifying the different types of content contained within. This could be used to create a more defined type hierarchy which could be used to better define basic font styles, etc.  Along with a basic color palette, this would greatly alleviate a lot of the styling issues.

## Refactor variable names to be more generic

Many of the current Less variables were created with names that closely resembled their original values (i.e. `@bg_gray: #F7F8F9;`) rather than their intended usage (`@header_background: #F7F8F9;`).

## Modularize existing .less files to be more granular 

The existing Less files are not always named according to what styles they contain — for example, styling for tables is contained in `typography.less`.  Breaking these into smaller and more granular files will greatly aid in both identifying where various styles exist, and overriding those styles in extended themes.
