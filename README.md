eRegulations Documentation
============

[eRegulations](http://www.consumerfinance.gov/eregulations/) is a web-based tool that makes regulations easy to find, read and understand with features such as inline official interpretations, highlighted defined terms, and a revision comparison view. This repository contains documentation for the project and can be viewed at <http://cfpb.github.io/eRegulations>

## Editing the documentation

The documentation uses [Jekyll](http://jekyllrb.com/) and our [DOCter](https://github.com/cfpb/DOCter) theme.

Be sure to have Jekyll and Kramdown installed:

```
gem install jekyll
gem install kramdown
```

Fork and clone the repo:

```
git clone git@github.com:ascott1/DOCter.git
cd DOCter
```
Run Jekyll:

```
jekyll serve --baseurl ''
```


### _config.yml

Options within the `_config.yml` file allow you to control the site's title, subtitle, logo, author information, and the left column navigation.
