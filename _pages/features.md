---
layout: default
title: Features
---
# Features

eRegulations includes an illustrated user guide that explains its features. See it live on the [CFPB](http://www.consumerfinance.gov/eregulations/about) and [ATF](https://atf-eregs.app.cloud.gov/about) instances.

## Current features

### Navigability

While regulations are traditionally represented as monolithic blocks of text, they contain a great deal of embedded structure. eRegulations teases out that structure and uses it to present the text in a clean, readable form.

### Inline interpretations

Many regulation paragraphs have official interpretations that have traditionally been displayed at the end of the regulation, forcing readers to jump back and forth between the regulation and its interpretation. eRegulations parses the interpretations for each paragraph, and displays them under the paragraph or section being interpreted.

### Definitions

We highlight words that have been defined in the regulation, and the user can click on the word and see its definition without scrolling to the part of the regulation that defines that word.

### Internal citations

Internal citations display as clickable links so users can quickly navigate between sections.

### Search

Users can search for keywords across various versions of a regulation.

### Versioning

Regulations are evolving documents and are often displayed as changes to the base text. We present whole versions of regulations for each set of changes and combine Final Rules that have a common effective date into one version.

### Comparing versions

Users can see how a regulation changed in a word-by-word or “redline” comparison view. Changes are expressed as additions (shown in green) or deletions (struck-through, in lighter gray).

### Filter by date

Users can view specific versions of a regulation by the effective date.

### Section-by-section analysis

The notices that compose a version of a regulation contain relevant analyses of the altered sections. We automatically pull that information out and make it accessible while reading the regulation text.

### Responsive design

The application design is responsive, adjusting to the device and screen size of the user.

### Comment on proposed rules

Proposed rules published by the [Federal Register](https://federalregister.gov) can be imported into our interface. Users can compare two versions side-by-side and comment on specific paragraphs or sections of the proposal. [Read more](/features/notice-and-comment).

## Goals for the future

We want other agencies, developers, and groups to use eRegulations and adapt it. Below are some enhancements we're hoping to develop in the future.

### More context and document types

eRegulations focuses on the Code of Federal Regulations right now, but regulations are only one part of an agency’s regulatory material. Related documents include both authoritative material (such as advisory opinions, rulings, and Federal Register notice preambles) and less-formal explanations that help people understand regulations and their requirements (such as guidebooks and FAQs).

eRegulations could better integrate with that related material (as well as the relevant statutes in the United States Code) to help users understand regulations.
A challenge is that each agency has its own collection of materials related to its regulations—with some types of documents in common and some unique to each agency. Some agencies use different names for similar types of documents.

A few examples:

* [CFPB](http://www.consumerfinance.gov/regulations/) includes "official interpretations" in its regulations (as an appendix to the main part of the regulation, all published together in the Code of Federal Regulations). CFPB also includes "section-by-section analysis" in its Federal Register notices. CFPB's eRegulations displays both of those types of material to help readers understand regulations.

* [ATF](https://www.atf.gov/rules-and-regulations) publishes "rulings" and "open letters" that clarify aspects of its regulations. It also publishes plain-language Q&As, newsletters, and guidebooks to help explain its regulations. ATF's eRegulations only has a small amount of cross-linking with related resources, and it could do a lot more in the future.

* [FEC](http://www.fec.gov/law/law.shtml) publishes "advisory opinions" and "Matters Under Review" that clarify aspects of its regulations, among other kinds of material.
Relatedly, we recently kicked off [an effort](https://github.com/18F/omb-eregs) to apply eRegs learnings to the Office of Management and Budget's policy documents.

### More flexibility

[Code and repositories](../technology/) explains this in more detail, but in short: the parser eats XML from many different sources and writes that to an API. The user interface (UI) then reads from that API. There is currently one UI for eRegulations, but the intent is for the parser to be usable outside of this one interface into regulations, and for the API to be usable outside of this one interface. For example, people could build a regulations authoring tool with a different UI. Some regulatory agencies have specific needs that may require a different UI.

The current codebase is somewhat tangled together, since there is just one UI right now, but supporting flexibility is an important ongoing goal.
