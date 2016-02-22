eRegulations Documentation
============

eRegulations is a web-based tool that makes regulations easier to find, read
and understand with features such as inline official interpretations,
highlighted defined terms, and a revision comparison view. This repository
contains companion documentation for the project and can be viewed at
<http://eregs.github.io/>

## Editing the documentation

The documentation uses [Jekyll](http://jekyllrb.com/) and the [DOCter](https://github.com/cfpb/DOCter) theme.

DOCter needs Jekyll and other dependencies to run locally. These can be installed with Bundler by running the following commands.

```
gem install bundler
bundle install
```

Run Jekyll:

```
bundle exec jekyll serve --watch --baseurl ''
```

Open it up in your browser: <http://localhost:4000/>


### _config.yml

Options within the `_config.yml` file allow you to control some of the site's
content and left column navigation.
