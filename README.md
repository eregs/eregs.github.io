eRegulations Documentation
============

[eRegulations](http://www.consumerfinance.gov/eregulations/) is a web-based tool that makes regulations easier to find, read and understand with features such as inline official interpretations, highlighted defined terms, and a revision comparison view. This repository contains documentation for the project and can be viewed at <http://cfpb.github.io/eRegulations>

## Editing the documentation

The documentation uses [Jekyll](http://jekyllrb.com/) and our [DOCter](https://github.com/cfpb/DOCter) theme.

DOCter needs Jekyll and other dependencies to run locally. These can be installed with Bundler by running the following commands.

```
gem install bundler
bundle install
```

Fork and clone the repo:

```
git clone git@github.com:cfpb/DOCter.git
cd DOCter
```
Run Jekyll:

```
bundle exec jekyll serve --watch --baseurl ''
```

Open it up in your browser: <http://localhost:4000/>


### _config.yml

Options within the `_config.yml` file allow you to control the site's title, subtitle, logo, author information, and the left column navigation.
