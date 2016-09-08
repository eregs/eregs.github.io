---
layout: default
title: eRegulations’ guidelines to writing rules and regulations
---

# eRegulations’ guidelines to writing rules and regulations

## Overview and checklist

- [ ] Follow the standard regulation outline structure.
- [ ] Add any bulleted or numbered lists to the main outline structure of your document.
- [ ] Use the built-in heading structure of your writing software in your document.
- [ ] Use headings consistently and wherever possible.
- [ ] Amend, revise, add to, or remove whole paragraphs.
- [ ] Reference the preamble when creating an amendment and vice versa.
- [ ] Write in language that the average member of the public will understand.

#### TABLE OF CONTENTS

TBD

## 1. What is eRegulations?

eRegulations is an open-source platform for making regulations easier to find, read, and understand. We digitally digest agency regulations and rules to present their built-in structure in a clean, readable form, including their changes over time. 

eRegulations Notice & Comment also provides a way for the public to comment on Notices of Proposed Rulemaking in a structured and more precise way. This makes it easier for commenters to respond to specific issues in the rule — down to the paragraph level — and allows agencies to efficiently sort and organize those comments. 

[You can learn more about the history, features, and background of the eRegulations platform at eregs.github.io.](https://eregs.github.io/)

## 2. Why is this document important?

### 2.1 Make regulations and notices easier and faster to parse
Following the formatting we outline in this document will allow the eRegulations platform to ingest your proposal or regulation without any problems. This will help to avoid extra manual work and customization on the developer’s part, significantly reducing your agency’s costs.

### 2.2 Regulatory consistency
Every agency has it’s own guidelines and tone for writing regulations, but the public sorts through regulations from many agencies in order to do one thing. The more alike regulations and rules are in structure across agencies, the lower the burden of understanding how to comply. Similarly, when in doubt and when possible, we encourage simple, plain language.

### 2.3 Close adherence to the Federal Register Document Drafting Handbook
First and foremost, we recommend following the [Federal Register Document Drafting Handbook](https://www.archives.gov/federal-register/write/handbook/chapters.html). By doing so, the eRegulations platform is able to enhance the data coming from the Federal Register and present it in a more contextual and human-readable format for your audience.

## 3. Formatting and structuring your rule

### 3.1 Format vs. structure
In regulation writing, document “semantics” refer to their _meaning_, as opposed to their _appearance_. For example, this document has two levels of headings. Their _appearance_ involves their font size, weight (for example, bold), etc. while their _semantics_ revolve around the structure they give to the document. For example, this section, “3.1 Format vs structure,” lives _inside_ the “3. Formatting and structuring your rule” section.  That is a _semantic_ structure.

The eRegulations platform is focused on the _structure_ of regulations, Federal Register notices, etc. We know how to split documents into separate pages, link between sections, show historical changes of a regulation over time, and so forth due to understanding the structure of the documents. Using and adding a level of formatting to meaningful headings and subheadings makes the rule easier for the eRegulations platform to parse and organize and for people to read. 

**We recommend that in your regulation writing, you avoid referring to specific formatting details** (such as “see the italic/underlined/bold text in paragraph (b)”) as the final representation may not display them the same way across all versions of your rule, and instead focus on the _semantic_ structure.

Similarly, keep in mind that the “idealized” rule (and the rule that gets printed) is one composed of headers, paragraphs, images, and tables. There is limited support for bulleted lists, nested paragraphs, emphasized text (and similar typographic formatting details), different types of indentation, and so forth. 

By focusing on the _semantic_ structure instead of typographic _formatting_ and limiting the rule to headers, paragraphs, images, and tables, you will guarantee the rule will appear consistent across print, federalregister.gov, and eRegulations.

### 3.2 File formats accepted by eRegulations

eRegulations uses the Federal Register’s XML data to display your agency’s _published_ rules and regulations. 

If you want to use eRegulations for your rule’s notice and comment period, or want to publish a document _before_ it is published in the Federal Register, we recommend the following file types in order of preference:

- _Ideally_
  - XML written in 
    - Document Type Definition (DTD), or 
    - A format that is written with the standards of the Federal Register in mind (i.e. using headers, paragraphs, tables, and images, and not lots of bullet points, indentations, and other styling and formatting)
  - Markdown HTML

- _Realistically_
  - Microsoft Word (.doc or .docx)
    - Using the Word’s built in heading structure within the document.

### 3.3 Structure

The eRegulations platform pulls out the structure of regulations and preambles to present the text in an easily readable format. This format allows for users to quickly skim through and find the paragraphs that apply to them. Building this structure properly is important because it allows users to link to specific citations and comment on specific paragraphs.

#### 3.3.1 Regulation structure

Please follow the Code of Federal Regulations recommended structure: 

**Title:** Broad subject area of regulations

**Chapter:** Rules of individual agency

**Part:** Rules on a single program **_[This is a “regulation” in the eRegulations platform.]_**

**Section:** One provision of program/function rules **_[Main level of navigation in eRegulations.]_**

**Paragraph:** Detailed, specific requirements

eRegulations primarily focuses on parts, sections, and paragraphs. The Federal Register allows for 6 levels of paragraphs:

- **Level 1:** (a), (b), (c), etc. § 303.1(a)
- **Level 2:** (1), (2), (3), etc. § 303.1(a)(1)
- **Level 3:** (i), (ii), (iii), etc. § 303.1(a)(1)(i)

> _[ Although it is possible to go past this point, the Federal Register recommends never going deeper than three levels. The Federal Register talks about [the benefits of limiting levels of paragraphs](http://www.archives.gov/federal-register/write/plain-language/readable-regulations.html). ]_

- **Level 4:** (A), (B), (C), etc. § 303.1(a)(1)(i)(A)
- **Level 5:** _(1)_, _(2)_, _(3)_, etc. § 303.1(a)(1)(i)(A)_(1)_
- **Level 6:** _(i)_, _(ii)_, _(iii)_, etc. § 303.1(a)(1)(i)(A)_(1)(i)_

#### 3.3.2 Keep to the outline structure

The regulation’s outline structure is a reader’s best friend. It creates hierarchical relationships between paragraphs, and therefore topics, allowing the reader to more easily focus their energy on sections that apply to them. 

The outline structure also fosters better citations. When paragraphs are “addressable”, they can be referenced by other paragraphs, notices, and documents. If a paragraph doesn’t fit into the structure, it’s not easy to reference, making it difficult for users to find. Further, the eRegulations platform allows readers to link directly to sections or paragraphs. 

**We recommend sticking very closely to the regulation outline structure** (or whatever outline structure you are using for your preamble). 

##### Be careful when using numbered lists.

Please do not use numbered lists that do not match up with your outline structure. Since the outline already has a hierarchical structure, numbered lists fit easily within that structure. This keeps the flow for readers while still communicating the 1, 2, 3 nature of your list. Although your drafting software will allow you to add a numbered list into your document, the eRegulations platform will not be able to properly pull it out because the numbers will seem like citations at the paragraph level. We want to keep citations working properly so readers have a better understanding of where they are in the document and how to tell someone else where to look.

##### Use bullets sparingly

Bullets can be great for breaking up paragraphs and clarifying text in way that’s visually easier to understand. However, the print version of the Federal Register document does not treat bullets differently than any other paragraph. For example:

![Bullets show up at the beginning of a paragraph with the same indent as any other paragraph in the three column print format.](https://cloud.githubusercontent.com/assets/4267825/18357276/537f82c0-75be-11e6-98f1-f5583e99111f.png)

The eRegulations platform currently follows the same pattern as the printed Federal Register document. We are working to pull out bullets in the future, but if your bullets can be similarly communicated within the outline structure (as discussed above re: [numbered lists](**ADD LINK TO ABOVE SECTION**)), **we recommend including these paragraphs in that structure.**

In addition, we recommend not using sub-bullets. Because bullets are treated the same as any other paragraph, they are very hard to follow in the print version of the document, and therefore, eRegulations. The hierarchical structure is stripped out. If your bullet has sub-bullets, consider another structure that only accommodates one level of bullets or builds your list into the larger outline structure of your document. 

##### One list at a time

In order to properly stick to the document’s outline structure, please avoid having more than one list in a paragraph level. For example:

![I. What is the agency proposing? Next paragraph, We are proposing a number of things: List starts, 1. First item, 2. Second item. Next paragraph, more discussion. Next paragraph, more discussion. Next paragraph, here’s another list: List starts, 1. A different set of items, 2. Second item.](https://cloud.githubusercontent.com/assets/4267825/18357551/6d0a4152-75bf-11e6-8132-724778ff9fa2.png)

Although the reader may be able to see which list belongs to which paragraph, the eRegulations platform cannot tell when one list ends, and the next begins. We recommend changing the above into something more structured so that both the platform and readers can follow your text more easily:

![I. What is the agency proposing? Next paragraph, We are proposing a number of things: List starts (built into the outline structure), 1. First item, 2. Second item. Next paragraph, more discussion. Next paragraph, more discussion. Next paragraph, II. Next topic, here’s another list: List starts (built into the outline structure), 1. A different set of items, 2. Second item.](https://cloud.githubusercontent.com/assets/4267825/18357771/301a1fdc-75c0-11e6-820a-ca7f04714190.png)

#### 3.3.3 Use headings wherever possible

The [Federal Register Document Drafting Handbook](https://www.archives.gov/federal-register/write/handbook/chapters.html) recommends the use of consistent headings at any paragraph level. Headings are essential to a good structured regulation or preamble. Headings group and explain topics to the public, so they know which paragraphs to read, and which don’t apply to them. Headings are the reason eRegulations fosters quick skimming and navigation throughout the document. 

The Federal Register handbook says, **“Present this information in language that the reader can easily understand, with descriptive headings to highlight and organize topics.”** Here is a good example of how this can work and look in the eRegulations platform:

![Image of CFPB's well organized § 1005.7 in eRegulations showing headings at every level of the outline structure.](https://cloud.githubusercontent.com/assets/4267825/18362267/18dc82fc-75d3-11e6-934e-9e0b8f8c3103.png)

We understand that it is not always feasible to have headings at every paragraph level. However, the Federal Register Handbook warns, **“Be consistent. If you use a heading for one paragraph, be sure to use a heading for all paragraphs at that level.”** Here are a few good examples of how this can work in the eRegulations platform:

![Image of ATF's well organized § 555.26 in eRegulations showing headings consistently used at the (a) and (b) levels of the regulation.](https://cloud.githubusercontent.com/assets/4267825/18362339/5fc39250-75d3-11e6-9588-fa663870cd32.png)

![Image of CFPB's definition of "Electronic fund transfer" showing headings at the (b) level and the (1) level but not the (i) level.](https://cloud.githubusercontent.com/assets/4267825/18362411/a049fb20-75d3-11e6-98d5-3e20daf414a2.png)

#### 3.3.4 Preamble structure

Federal Register notices do not have as defined of a structure as regulations. However, a good, and easily parsable, preamble in a Notice of Proposed Rulemaking should follow the outline structure and heading advice above. 

Although preambles’ paragraphs are a little more freeform than regulation paragraphs, the structure is extremely important for the public to understand what the agency wants comments on. Here is a good example of how this may look in the eRegulations platform:

![Image showing EPA's well organized preamble using headings at all three (III), (A), and (1) levels. ](https://cloud.githubusercontent.com/assets/4267825/18362615/7c2b5ba2-75d4-11e6-8083-9d014fe4bac3.png)

This rule follows this pattern throughout. As you can see in the table of contents. This preamble uses questions as headers as much as possible. In addition, they separate background paragraphs from paragraphs about what the current rule is proposing.

![Image of EPA's table of contents showing headings in the form of questions that organize each (A), (B), (C), level of the document. EPA continues to use question headings at many of the (1), (2), (3) next level down. ](https://cloud.githubusercontent.com/assets/4267825/18362749/04a4edc2-75d5-11e6-8744-5c9f5c872766.png)

## 4. Changing regulation text

### 4.1 Language describing the changes

> _“For extensive changes, revise the text in full rather than prepare fragmentary amendments. The
reader will then have the complete text of the amended unit.”_ - [Chapter 1.13 of the Federal Register Document Drafting Handbook](https://www.archives.gov/federal-register/write/handbook/chapter-1.pdf)

The goal of the eRegulations comparison tool is to show how regulations have changed over time or how they will change in the future. We are able to automate this process by following the guidelines the Federal Register has laid out in their Handbook. However, computers have a harder time understanding certain commands than humans do. Following the below recommendations will save you development time for your eRegulations instance, and help give readers more context around the changes you are trying to make.

#### 4.1.1 Revise the entire paragraph by default

Even if you are only revising a word or a sentence, **we recommend revising the entire paragraph**. The computer will easily be able to compare the new text to the old text and show the differences in the eRegulations platform. Something like “change the fifth word in paragraph (b)” is hard for computers to get right, and may require manual intervention by an eRegulations developer. 

Here is one example of a change that is hard to parse: "In § 478.72, add a new fifth sentence to read as follows:" At first glance, that seems like a simple instruction, but what does it actually mean? It could be saying, "insert this sentence and shift everything down,” or could it mean, "replace the fifth sentence"? It could also potentially mean, "add a new sentence to the end of the paragraph." Showing the full revised paragraph adds context for both the computer parsing your regulations and those of your readers who are looking at the printed rule. 

#### 4.1.2 Using specific keywords

The eRegulations platform follows the Federal Register’s [specific amendatory terms (Chapter 1.13)](https://www.archives.gov/federal-register/write/handbook/chapter-1.pdf) very closely to create the comparison between the old and new regulation. We recommend following those guidelines and using words like "revise", "add", "remove" as opposed to "change", "create", "delete", etc. when amending regulation text in a notice of proposed rulemaking.

The following is a list of words from the Federal Register’s [guidelines](https://www.archives.gov/federal-register/write/handbook/chapter-1.pdf) that the eRegulations platform recognizes. The eRegulations platform does not currently recognize the words that are crossed out. If you use one of those words, it will require manual intervention by an eRegulations developer. 

- Add, Added, Adding
- Redesignate, Redesignated, Redesignating
- Remove, Removed, Removing
- ~~Republish~~, ~~Republished~~, ~~Republishing~~
- Reserve, ~~Reserved~~, Reserving
- Revise, Revised, Revising
- ~~Withdraw~~, ~~Withdrawn~~, ~~Withdrawing~~

#### 4.1.3 Examples 

**Good:** “Section 262.24 is amended by revising paragraphs (c) and (g) to read as follows:”

Why:
- Context: “Section 262.24” is front and center
- Which paragraphs are being modified is clear
- Whole paragraphs are being modified
- Use of “revising”

**Good:** “Subpart FF is added to read as follows:”

Why:
- Clear which entity is being modified (here, a subpart)
- Use of “added”

**Bad:** “Change the fifth word in the eighth paragraph to ‘cromulent’”

Why:
- Context is difficult to determine — we need to count paragraphs manually
- Counting words is even more of a challenge to handle automatically
- Spelling out phrases leaves room for interpretation (think spacing, comma placement, etc.)

### 4.2 Cross referencing from the preamble

One of the biggest pain points for readers of a proposed rule is the connection points between where a change is discussed in the preamble and the actual new language. In our user research, many readers asked for this feature, but the eRegulations platform cannot make a connection automatically unless the proper citations are written into the document. 

When discussing why your agency is making a specific change to a regulation, **we recommend referencing the citation that is being changed in addition to the numbered amendment in the notice**. For example: 

 “The regulatory requirements for [this new item] are proposed at § 264.71(b) in amendment 10 of this proposed rule.”

When amending regulatory text in your proposed rule, **we recommend referencing the section of the preamble where you discuss why you are making the change in your instructions**. For example:

“10. As discussed in Section III.A.3 of this proposed rule, § 271.12 is amended by adding paragraph (k) to read as follows:”

## 5. Benefits of plain language

### 5.1 Everyone gains

> _“Readable regulations help the public find requirements quickly and understand them easily. They increase compliance, strengthen enforcement, and decrease mistakes, frustration, phone calls, appeals, and distrust of government. **Everyone gains.**”_ - [Part II Making Regulations Readable, Federal Register Document Drafting Handbook](http://www.archives.gov/federal-register/write/plain-language/readable-regulations.html)

U.S. government regulations are for everyone. The content they contain should therefore be as straightforward and clear as possible.

We recommend avoiding formal or long words when easy or short ones will do. For example, use _buy_ instead of _purchase_, _help_ instead of _assist_, _about_ instead of _approximately_, and so on.

We lose reader’s trust and understanding if we write using long, confusing, “government” language. We also lower compliance with regulations and create more phone calls and inquiries to agency staff when readers cannot understand the regulation or legal guidance on first reading.

### 5.2 It’s the law

The [Plain Language Act of 2010](https://www.gpo.gov/fdsys/pkg/PLAW-111publ274/pdf/PLAW-111publ274.pdf) reads, with our emphasis, as follows:

> (2) COVERED DOCUMENT. —The term ‘‘covered document’’—
>
> (A) means any document that—
>
> (i) is necessary for obtaining any Federal Government benefit or service or filing taxes;
>
> (ii) provides information about any Federal Government benefit or service; or
>
> (iii) **_explains to the public how to comply_** with a requirement the Federal Government administers or enforces;
>
> (B) includes (whether in paper or electronic form) a letter, publication, form, **_notice_**, or instruction; and
>
> (C) does not include a regulation.
>
> (3) PLAIN WRITING.—The term ‘‘plain writing’’ means writing that is clear, concise, well-organized, and follows other best practices appropriate to the subject or field and intended audience.”

**This law applies to the preamble of Federal Register notices,** which explain how and why users need to comply with the new regulation. 

Although this law does not apply directly to regulations, there are three Executive Orders ([E.O. 12866](http://www.plainlanguage.gov/populartopics/regulations/eo12866.pdf), [E.O. 12988](http://www.plainlanguage.gov/populartopics/regulations/eo12988.pdf), and [E.O. 13563](https://www.gpo.gov/fdsys/pkg/FR-2011-01-21/pdf/2011-1385.pdf)) that promote the use of plain language in regulations. And, the benefits of applying plain language to regulation text (as it changes over time) can be measured in industry compliance and agency staff time spent responding to inquiries. 

If you are interested in the benefits and history of plain language guidence for regulations, plainlanguage.gov has a [good explanation](http://www.plainlanguage.gov/populartopics/regulations/index.cfm).

### 5.3 A few tips and resources

- [Part II Making Regulations Readable, Federal Register Document Drafting Handbook](http://www.archives.gov/federal-register/write/plain-language/readable-regulations.html) gives great advice (specific to regulation writing) on how to write clear rules. They have seven writing techniques that can improve the look and sound of a rule. Their top two pieces of advice are:
  - Use questions in section headings
  - Use "You" for whoever must comply

- [Federal Plain Language Guidelines](http://www.plainlanguage.gov/howto/guidelines/FederalPLGuidelines/index.cfm) 

- The Federal Register explains how to [rewrite a short rule, step by step](http://www.archives.gov/federal-register/write/plain-language/short-rule-1.html).

- [18F’s Content Guide on Plain Language](https://pages.18f.gov/content-guide/plain-language/)

- The average American reads at a 7th or 8th grade level. It can be hard to reach that level in a complicated document like a regulation, but it is good to aim for a level that most people can easily understand. Tools like the [Hemingway Editor](http://www.hemingwayapp.com/) or [Readability Score](https://readability-score.com/text/) allow users to check their text for the current reading level and pulls out particularly tricky sentences and words that are worth editing.


