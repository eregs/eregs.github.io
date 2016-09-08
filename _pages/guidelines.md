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





