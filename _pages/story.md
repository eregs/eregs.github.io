---
layout: default
title: History, present, and future
---

# History, present, and future

We would like other agencies, developers, and groups to use eRegulations and adapt it. Here's some insight into the current status of the project and where it's going.

# History

[CFPB released its initial version of eRegulations in 2013](http://www.consumerfinance.gov/blog/making-regulations-easier-to-use/), and [18F and ATF began reusing it for ATF in 2015](https://18f.gsa.gov/2015/12/09/an-open-source-government-is-a-faster-more-efficient-government/).

A few news clippings that also discuss motivations for eRegulations:

* [October 2013, BloombergView](http://www.bloombergview.com/articles/2013-10-29/one-federal-website-that-works): "Texts of official government rules are notoriously difficult to follow. Multiple cross-references to other rules make it necessary to consult many different resources. Experienced rule readers can find official interpretations; others can’t. CFPB’s new user-friendly site makes all available information visible and easily accessible...By focusing on users’ experience of the site, they built something that works well for real people. And the platform will constantly be upgraded because it’s open source -- meaning that any agency or company can adopt it free and improve on it."

* [October 2013, Administrative Conference of the US](https://www.acus.gov/newsroom/administrative-fix-blog/cfpb%E2%80%99s-eregulations-tool-promises-help-users-navigate-federal): "By opening eRegulations up to suggestions and improvements from the public, CFPB is allowing hands-on contribution to the debate over what sources are appropriately considered as a part of regulatory interpretation."

* [January 2014, Nextgov](http://www.nextgov.com/emerging-tech/2014/01/want-make-digital-government-work-hire-your-own-coders/76223/): "By using hypertext and modern Web design, they thought, regulators could make proposed rules more available and comprehensible to the general public and reduce busy work for industry attorneys and activists who spend hours parsing through regulations each day...'Where it’s going really depends on what we hear from the public, largely from the compliance industry and other folks that have to use regulations on a day to day basis as part of their jobs,' Yuda said. 'What we hear from those people will guide not just how we go forward with this but whether we go forward. If we hear it’s useful, then we’ll continue. If we hear that it’s not, then we have limited resources and we need to invest those in areas where we’re going to be providing value to the American public.'"

# Present and future

## Scope of eRegulations

eRegulations only covers Code of Federal Regulations parts right now. But each agency's regulations are only one piece of their regulatory material.

Each agency creates a lot of related documents that aren't included in the Code of Federal Regulations: both authoritative material (such as advisory opinions, rulings, and Federal Register notice preambles) and less-formal explanations that help people learn what they need to know (such as guidebooks and FAQs).

eRegulations could better integrate with that related material (as well as the relevant statutes in the United States Code) to help users understand regulations.

A challenge is that each agency has its own collection of materials related to its regulations - with some types of documents in common with other agencies and some unique to one agency. Some agencies use different names for similar types of documents.

A few examples:

* [CFPB](http://www.consumerfinance.gov/regulations/) includes "official interpretations" in its regulations (as an appendix to the main part of the regulation, all published together in the Code of Federal Regulations). CFPB also includes "section-by-section analysis" in its Federal Register notices. CFPB's eRegulations displays both of those types of material to help readers understand regulations.
* [ATF](https://www.atf.gov/rules-and-regulations) publishes "rulings" and "open letters" that clarify aspects of its regulations. It also publishes plain-language Q&As, newsletters, and guidebooks to help explain its regulations. ATF's eRegulations does not integrate those types of material, but it could in the future.
* [FEC](http://www.fec.gov/law/law.shtml) publishes "advisory opinions" and "Matters Under Review" that clarify aspects of its regulations, among other kinds of material.

## How it works

[Code and documentation](technology/) explains this in more detail, but in short: the parser eats XML from many different sources and writes that to an API. The UI then reads from that API.

There is currently one UI for eRegulations, but the intent is for the parser to be usable outside of this one interface into regulations, and for the API to be usable outside of this one interface.

For example, people could build a regulations authoring tool with a different UI. Some regulatory agencies have specific needs that may require a different UI.

The current codebase is somewhat tangled together, since there is just one UI right now, but supporting flexibility is an important ongoing goal.

## Advice for ongoing cross-agency development

Everyone is free to use and adapt eRegulations as they wish. We encourage you to build your adaptation in the open (and with a public domain + CC0 license), and to build it in close coordination with other contributors, so everyone can benefit from each other's work.

### Working with the shared codebase and building agency-specific features

The procedure if you develop a feature that would be more platform-oriented: **regulations-core**, **regulations-site**, and **regulations-parser** are the core platform; they're shared code. We don't have a very good "raw" eRegulations right now, though we're slowly moving there. "Raw" eRegulations is basically CFPB eRegulations right now.

At this point, you would probably never run **regulations-site** or **regulations-core** on their own. Instead, they're libraries - you can modify them as libraries. Effectively, you point the wrapper to local checkouts.

In general we are not extending the core repo further when we make changes to an agency-specific setup.

### Share or fork the codebase? Specific features or generalizable features?

Each reuse of eRegulations faces a tradeoff: fork the codebase, or make the effort to work to share the main codebase? Build features specific to the agency, or try to build more generically reusable features even if it takes more time?

It's important to plan to use the shared codebase and to build features that are relatively reusable — and to balance this vision with the pragmatic needs of your budget.

The work to make it generalizable is good for each agency. Each agency benefits from the generalizing work of previous agencies, and all clients will themselves benefit when, inevitably, they produce regulations in the future with quirks that will be easier to handle within an extensible/generalizable system.

We are not sure yet how long-term cross-agency maintenance will work. We'll figure it out together.
