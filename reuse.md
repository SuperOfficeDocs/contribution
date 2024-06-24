---
uid: content-reuse
language: en
title: Content reuse
description: Introduction to content reuse and singlesourcing
topic: concept
date: 08.1.2022
author: Bergfrid Dias
---

# Content reuse

Content reuse is to use the same pieces of content in multiple places without copying. It works like this:

1. Write a piece of content and save it in a common place.
2. Embed this content in one or more locations **by reference**.
3. Any changes to the content can be done in one place and the updates are automatically applied wherever that piece is used.

## Benefits

You can create new content from existing pieces. By doing this:

* Content is more consistent.
* The content creation process is sped up and you avoid duplicating work.
* It is easier and faster to update content.
* You avoid mistakes introduced by extensive copying and pasting.
* You facilitate cost-effective translation. Even a slightly altered copy-pasted text may not be recognized as already translated.
* You reduce redundancy. Information (source) is stored only once.

## What can I reuse?

What constitutes a reusable chunk depends on your granularity.

In topic-based writing, a topic could for example be *How to create a sale* while another could be *What is a sales guide*. These are both candidates to be used in the user guide and the FAQ. For SuperOfficeDocs, a topic is the equivalent of a webpage.

Often, you identify smaller pieces of information as recurring. For example:

* A note stating which license a task requires.
* A single task step repeated in multiple procedures, such as "Click the **Save** button".
* A list of something, such as follow-up statuses.

These pieces go by many names: snippet, fragment, chunk, component, excerpt. In the following, let's call them **fragments** as a reminder that they are not published on their own. They are designed to be embedded into other content.

## Problems

* Someone changes reused content to fit their context and ignores other places the content is used. Authors need to understand the impact of the changes they make.

* Relative links in a fragment or topic might not resolve in all contexts. If output B is a subset of output A, any link within B topics will break if it targets a topic in A that is excluded in B.

* The more fragments you stitch together in a topic, the harder it becomes to read the source file. The content becomes more abstract and technical to work with.

* Duplicate pages. See details below.

### Using the same topic as a whole multiple times in the same output

A **true duplicate** has no benefits. Cutting duplicate content pages improves UX.

* It confuses users who see the same page multiple times in the search results.
* It is [bad for SEO][1].
* It is bad for link equity.

A user generally finds content in one of these ways:

* Direct link from Help, FAQ, or another topic.
* Via a search engine such as Google or Bing.
* Search on your site.
* Browsing your site.

In the first case, you have direct control over where to send the user and you gain nothing from curating duplicates. For both internal and external search, duplicates are a minus. That leaves us with site navigation.

Linking to a topic from multiple landing pages is a plus. It builds link equity. If a user visits page A and you think they should also consider page B, link to it directly instead of placing a duplicate of B next to A in the TOC. With curated landing pages you can provide a much broader picture of an area of interest than you can with structural placement alone.

## Reuse strategy

Without a strategy, content reuse can quickly become confusing and frustrating.

If people can't find the reusable topics and fragments, they'll rewrite it from scratch.

It is a good practice to sign-post reusable content. For SuperOfficeDocs we use folders named *includes*. Establishing a file naming convention doesn't hurt either.

There is a compromise between usability for contributors and optimization for hard-core authors. Just because you can extract it, doesn't mean you should. What you want to avoid is making your source so complex and cryptic that it requires specialized training to do something as trivial as fixing a typo. If people are overwhelmed, they stop contributing.

## Writing for reuse

Writing for reuse takes skill and practice.

A **reusable topic** should cover only one subject (the principle of single responsibility). The more you cram into a topic, the more you anchor it to a specific context, the harder it becomes to reuse it.

Minimize similar content. Instead of having 3 similar pages, either consolidate them into a single page *or* expand each page to make it more distinct.

**Fragments** should be placed in dedicated folders and formulated more generic than you'd normally would without reuse. For example, if you can reach a page in 3 different ways, it's better to say "Go to the **Sale** page" rather than stating a specific navigation path. The latter significantly reduces the reuse potential.

**Dos:**

* Say the same thing, the same way, everywhere you say it.
* Aim to make your topics stand alone without breaking the single responsibility principle.
* Make it generic instead of specific. Include as much information as the end user needs while keeping it generic enough to be applicable in multiple contexts.
* Standardize terminology. Use consistent grammar and style.
* Favor brevity and simplicity.

**Don'ts:**

* Don't Repeat Yourself (DRY): if you catch yourself thinking you've written something before, stop and look for reuse opportunities.
* Avoid contextual phrases such as "in the previous section".
* Don't overdo it. How small is small enough? How small is too small?
* Don't nest fragments.

If a piece of information is essential to completing a task or understanding a concept, it should be embedded. However, avoid detours. Instead of going off on a tangent, include a very brief summary and then link to a page with more details. Websites are navigated through links. Don't burden the reader with excessive blocks of text.

## Finding content to reuse

Reusable content should be easy to find. Use **domain modelling**: have all topics about one subject in one place.

**After** optimizing content for reuse, you can perform **targeted searches** to find content to reuse in a given topic. You probably need to comb through the results to decide what is suitable and what's not. Sorry, but there is no magic button. If you want to become efficient in reuse, learn how to search your source.

<!-- Referenced links -->
[1]: https://developers.google.com/search/docs/advanced/guidelines/duplicate-content

<!-- Referenced images -->
