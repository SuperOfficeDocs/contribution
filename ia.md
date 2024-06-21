---
uid: info-architecture
language: en
title: Information architecture
description: Introduction to information architecture
keywords: IA, structure, cognitive load
topic: concept
date: 08.1.2022
author: Bergfrid Dias
---

# Information architecture

> Information architecture is about helping people understand their surroundings and find what they’re looking for, in the real world as well as online. [(Information Architecture Institute)][1]

You could also say that IA is the **practice of organizing content effectively**. It is tightly coupled with UX, web design, and content strategy.

> [!NOTE]
> While the output of IA work is often a site map, IA is **not** a synonym for site navigation.

When considering IA, it is vital to understands how people actually use content and how the structure should function to support that. The importance of structure increases with the amount of content. Without a solid foundation, UX in general and navigation in particular will crumble.

## How users find info on the site

More than half of users will use a different entry point than the home page.

* Direct link from F1 or FAQ
* Direct link from a forum or blog post
* User knows exactly what they are looking for and uses either a search engine or your local search
* User wants to explore certain keywords (fuzzy goals)
* User wants to follow a guided learning path (focused study)
* User looks for a solution without understanding the problem (this is when they might resort to live chat or contact support)
* User wants to find something they accessed earlier

Ask yourself:

* What is the flow of users through our website?
* What are these users going to do on the website?
* Once on a page, are they more likely to navigate using the left menu or rely on related links?

## Mental models

Mental models are **assumptions** of where information should be. Different users have different models.

Ask yourself:

* What does the user expect to see?
* Do people know where to go to look for content? Where would you go to... ?

## Taxonomy and metadata

Taxonomy deals with grouping things together. Metadata is used to tag content.

Categories should be clearly named and mutually exclusive **logical buckets**. A poly-hierarchy classification accommodates different mental models. However, it dilutes categories and you should do this only when you know that the user will actually look for it in both places.

Ask yourself:

* What are the content areas?
* What is the site content and functionality?
* What is the relationship between these?

## Navigation and hierarchies

Which type of navigation is suitable depends on the shear volume of content and how you answered the above questions.

| Type | Works best for | Suitable for docs? |
|---|---|---|
| All info on a single page | Seamless UX with limited content| no |
| Flat structure with one level of navigation | 10 or fewer pages | no |
| An index of all pages in a single location | Very narrow topics | no |
| Central hub (daisy structure) | Smaller sites with| partially |
| Strict hierarchy (pages accessible only from their parent) | Educational content where you want to enforce a reading order | partially |
| Multidimensional hierarchy | Extensive content with multiple ways to access a page | yes |

In its most basic form a multi-hierarchy offers access from a page's parent plus a central navigation menu. In contrast, Wikipedia-style sites are a web of interrelated content.

SuperOfficeDocs uses a multidimensional hierarchy with both a central left navigation menu, curated landing pages, and links to related content. The start page of a folder is always *index.md* or *index.yml*. Both render as *index.html*.

We do not however expose the full site map in a single navigation tree. That would overwhelm the users and violate the principle of an inverted-L navigation having max 4 tiers.
Instead, we use the home page as the hub in a daisy structure for featured content and popular areas of interest.

Most areas of interest have their own landing page, which serves as a level 2 hub. As a result, you can both drill down from the top and browse within your local context. Links in the hub are not limited to the left menu.

When a certain learning path is desired, we use tutorial type pages, which lets the user step through a planned progression.

## Future proofing

Rethinking your IA is extensive work and is not something you do every six months. Even if it's "just" rewiring your sitemap and republishing, it has huge impact on the users. Every page moved or relabelled represents a broken link to someone. And you are basically asking them to re-learn to navigate your site over and over again. Not exactly great UX.

Thus, you should future proof your IA and make it as sustainable as you possibly can.

Assume content will grow. The structure should be scalable. If the fourth level of your menu is already overflowing at launch, revising the structure soon becomes necessary.

If you mimic the structure of a product or corporate organization, changes in those will trigger IA revisions unless you settle for being outdated. You can still explain those structures to you user, and you should, without basing your taxonomy on them. With the ongoing consolidation of client applications and transition to cloud-only, changes are inevitable.

How a user performs a task today might differ how it will be done in the future. Locking the structure to a workflow has the same challenges as mimicking a product. The same goes for user type or role.

Domains are more evergreen and you can always create pages with super-procedures and overviews of tasks per role and so on. This way, the information becomes content you can revise as any other concept, task, or reference.

## Domain modelling

Topic-based navigation is often the main navigation for a site. Most users think in terms of objects first and task second.

**For authoring**, grouping by domain provides close proximity of related content. By keeping it all in one location:

* Author productivity increases
* It's easy to find pertinent content you need to update
* It's easy to decide where to store new content
* Relative links are short/local

**For content reuse**, findability increases making it easier to reuse rather than recreate/duplicate content.

* Domain-specific reusable content and screenshots are close to where they're used.
* Without domain modelling, variants of the same content appear in multiple buckets.

**For translation**, this means that new and changed files are already grouped together. (This is also a plus for version control in general.)

<!-- Referenced links -->
[1]: http://www.iainstitute.org/

<!-- Referenced images -->