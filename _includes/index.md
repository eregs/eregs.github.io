## Features

Some of the main features of the tool are:

- #### NAVIGABILITY.
While regulations are traditionally represented as monolithic blocks of text, they contain a great deal of embedded structure. eRegulations teases out that structure and uses it to present the text in a clean, readable form.

- #### INLINE INTERPRETATIONS.
Many regulation paragraphs have official interpretations that have traditionally been displayed at the end of the regulation, forcing readers to swap back and forth between the regulation content and interpretation at the end. eRegulations parses the interpretations for each paragraph, and displays them right under the paragraph/section being interpreted.

- #### DEFINITIONS.
We highlight words that have been defined in the regulation, and the user can click on the word and see it's definition without scrolling to the part of the regulation that defines that word.

- #### INTERNAL CITATIONS.
The parser parses out all internal citations in the regulation, and we display them as clickable links allowing easy navigation within a regulation.

- #### SEARCH.
We provide the ability to search for phrases across various versions of a regulation.

- #### ALTERNATE VERSIONS OF THE REGULATIONS.
Regulations are evolving documents and are often displayed as changes to the base text. We present whole versions of regulations for each set of changes (We combine Final Rules that have a common effective date into a version).

- #### COMPARING VERSIONS.
We show the difference between whole versions of regulations in a "redline" or word-by-word comparison view. All changes are expressed as additions (shown in green) or deletions (struck-through, lighter gray). This view clearly shows how a regulation changes.

- #### RETRIEVE BY EFFECTIVE DATE.
A user can also enter in a date, and retrieve the version of the regulation effective at that point in time.

- #### SECTION-BY-SECTION ANALYSIS.
The notices that compose a version of the regulation contain relevant analyses of the altered sections. We automatically pull that information out and make it accessible while reading the regulation text.

- #### RESPONSIVE DESIGN.
The application design is responsive, adjusting to the device and screen size of the user.

## Architecture

There are three parts to the eRegulations application: a parser that converts regulation text into data ([regulations-parser](https://github.com/cfpb/regulations-parser)), an API that hosts this data ([regulations-core](https://github.com/cfpb/regulations-core)), and a webapp which uses the data from the API to construct beautiful and usable regulations ([regulations-site](https://github.com/cfpb/regulations-site)).

One would typically run the parser against a regulation once (for each version) to populate the API with all the necessary data. regulations-site would then use regulations-core to as necessary to display regulations.

## Technology

regulations-parser is written in Python.

regulations-core is a Django and Haystack application.

The regulations-site front-end is a Backbone.js application nested within AMD modules using Require.js. We also use a Grunt-based build system with Jasmine for unit testing. On the back-end regulations-site is a Django application.

## Open Source and Contributing

We invite contributions to any part of the application. The project is in the public domain, and all contributions to it will be released as such. By submitting a pull request, you are agreeing to waive all rights to your contribution under the terms of the [CC0 Public Domain Dedication](http://creativecommons.org/publicdomain/zero/1.0/).

If you contribute the open source work of others, please mark it clearly in your pull request.

