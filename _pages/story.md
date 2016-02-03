---
layout: default
title: History, present, and future
---

# History, present, and future

# History

A few news clippings that discuss the motivations for eRegulations:

[October 2013, BloombergView](http://www.bloombergview.com/articles/2013-10-29/one-federal-website-that-works): "Texts of official government rules are notoriously difficult to follow. Multiple cross-references to other rules make it necessary to consult many different resources. Experienced rule readers can find official interpretations; others can’t. CFPB’s new user-friendly site makes all available information visible and easily accessible...By focusing on users’ experience of the site, they built something that works well for real people. And the platform will constantly be upgraded because it’s open source -- meaning that any agency or company can adopt it free and improve on it."

[October 2013, Administrative Conference of the US](https://www.acus.gov/newsroom/administrative-fix-blog/cfpb%E2%80%99s-eregulations-tool-promises-help-users-navigate-federal): "By opening eRegulations up to suggestions and improvements from the public, CFPB is allowing hands-on contribution to the debate over what sources are appropriately considered as a part of regulatory interpretation."

[January 2014, Nextgov](http://www.nextgov.com/emerging-tech/2014/01/want-make-digital-government-work-hire-your-own-coders/76223/): "By using hypertext and modern Web design, they thought, regulators could make proposed rules more available and comprehensible to the general public and reduce busy work for industry attorneys and activists who spend hours parsing through regulations each day...'Where it’s going really depends on what we hear from the public, largely from the compliance industry and other folks that have to use regulations on a day to day basis as part of their jobs,' Yuda said. 'What we hear from those people will guide not just how we go forward with this but whether we go forward. If we hear it’s useful, then we’ll continue. If we hear that it’s not, then we have limited resources and we need to invest those in areas where we’re going to be providing value to the American public.'"

# Present and future

## Scope of eRegulations

eRegulations only covers Code of Federal Regulations parts right now. But useful interfaces to regulations are only one part of the complex information architecture needs of regulatory agencies.

The future of eRegulations could better integrate related material such as Federal Register notices and more. Each agency has its own collection of supplemental material around its regulations - for example:

* CFPB has "section-by-section analysis" provided as appendices to its regulations (within the CFR).
* ATF has "rulings" and "open letters" clarifying aspects of its regulations, as well as plain-language Q&As, newsletters, and guidebooks that help explain its regulations.
* FEC has "advisory opinions" and "Matters Under Review" clarifying aspects of its regulations.


## How it works

In short: the parser eats XML from many different sources and writes that to an API. The UI then reads from that API.

There is currently one UI for eRegulations, but the intent is for the parser to be usable outside of this one interface into regulations, and for the API to be usable outside of this one interface.

For example, people could build a regulations authoring tool with a different UI. Some regulatory agencies have specific needs that may require a different UI.

The current codebase is somewhat tangled together, since there is just one UI right now, but supporting flexibility is an important ongoing goal.

## Advice for ongoing cross-agency development

Everyone is free to use and adapt eRegulations as they wish. We encourage you to build your adaptation in the open (and with a public domain + CC0 license), and to build it in close coordination with other contributors, so everyone can benefit from each other's work.

### Working with the shared codebase and building agency-specific features

The procedure if you develop a feature that would be more platform-oriented: -core, -site, and -parser are the core platform; they're shared code. We don't have a very good "raw" eRegs right now, if that makes sense (though we're slowly moving there). "Raw" eRegs is basically CFPB eRegs right now.

At this point, you would probably never run regulations-site or -core on their own. Instead, they're libraries - you can modify them as libraries. Effectively, you point the wrapper to local checkouts.

In general we are not extending the core repo further when we make changes to an agency-specific setup.

### Share or fork the codebase? Specific features or generalizable features?

Each reuse of eRegulations faces a tradeoff: fork the codebase, or make the effort to work to share the main codebase? Build features specific to the agency, or try to build more generically reusable features even if it takes a little more time?

It's important to plan to use the shared codebase and to build features that are relatively reusable - and to balance this vision with the pragmatic needs of your budget.

The work to make it generalizable is good for each agency; each agency benefits from the generalizing work of previous agencies, and for example, all clients will themselves benefit when, inevitably, they produce regulations in the future with quirks that will be easier to handle within an extensible/generalizable system and would be much harder without that generalizability.

We are not sure yet how long-term cross-agency maintenance will work. We'll figure it out together.

