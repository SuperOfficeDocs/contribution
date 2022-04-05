---
uid: how_to_create_tutorial_page
title: How to create a tutorial page
locale: en
so.topic: reference
so.date: 04.04.2022
so.author: AnthonyYates
---

# How to create a tutorial page

This section teaches how to create a step-by-step tutorial page. The purpose of a tutorial page is to break down large tasks into bite-sized chunks.

![Overview][overview]

## YAML Content

The following example yaml represents a tutorial page, consisting of 5 top-level properties.

1. Page type declaration **(YamlMime:Tutorial)**
2. Unique identifier
3. Metadata
   1. Title displayed on the page
   2. Description displayed on the page
   3. Audience (for future use)
   4. so.topic (for future use)
   5. so.date
   6. level (for future use
4. Items: collection of 2 or more steps (minimum of 2).
   1. Title (displayed as step title)
   2. Duration (estimated in minutes)
   3. Content (readable article step text)

There must be 2 or more steps, where each step is delineated by a combination of title, durationInMinutes and content elements. Below there are two step examples, Prerequisites and Get example.

Step titles are not ste descriptions. Use as few words as possible, no more than 3! If nothing better, use Step 1, Step 2, Step 3 etc.



```yaml
### YamlMime:Tutorial
uid: tutorial-create-online-crm-application
title: Tutorial - Learn how to create an Online CRM App.

metadata:
  title:  Tutorial - Learn how to create an Online CRM application.
  description: In this tutorial, you'll learn how to create an application that connects to your SuperOffice CRM Online tenant.
  audience: Developer    # reader audience Developer | Consultant
  so.topic: tutorial     # tutorial | how-to-guide | architecture
  so.date: 03/13/2022    # created / updated date
  level: Intermediate    # intended user level

items:

- title: Prerequisites
  durationInMinutes: 3
  content: |
    You must have:
    * a [tenant](../terminology.md) and user with admin privileges for testing sign-in.

    # ... removed for brevity

- title: Get example 
  durationInMinutes: 2
  content: |
    **Clone** or **download** the [SuperOffice.DevNet.RazorPages](https://github.com/SuperOffice/devnet-oidc-razor-pages-webapi) from GitHub.

    `git clone https://github.com/SuperOffice/devnet-oidc-razor-pages-webapi.git`

    In Visual Studio, go to the *Source* directory and **open** the *SuperOffice.DevNet.RazorPages.sln* file.

    ![image8z7wl.png -screenshot](../media/image8z7wl.png)   
```

### Content Options

Writing markdown in markdown files (with a .MD extension) is a much better experience than writing markdown in yaml files. Therefore, as an alternative to writing markdown in the content section of each yaml step, consider writing markdown content in markdown files that are then "included" in each content section.

In the following example, notice how the content property of step one (Introduction) is normal, but that steps 2 (Prepare parameters) and 3 (Convert) are short, and only specify an "Include" file.

In these cases, it's recommended to place all dependant markdown files in a local folder called includes. Then simply reference these by filepath:

`includes/steps/prepare-parameters.md`

How files are organized in the includes folder is up to you. [Include files][includes] are a great way to bring in markdown content without having to edit it directly in the yaml file, with edits done in your preferred markdown editor.

```yaml
items:
- title: Introduction
  durationInMinutes: 1
  content: |
    This Windows application retrieves a list of activities for the past 6 months of the logged-in user. It also supports filtering the activities based on user input.

    Steps 2 and 3 explain how to retrieve activity information using the Activity Archive Provider and convert the retrieved information into a format that can be displayed in a data grid.
    The code segments use the **SuperOffice.CRM.ArchiveLists.ActivityArchiveProvider** to retrieve the activities.
- title: Prepare parameters
  durationInMinutes: 3
  content: |
    [!include[Content: prepare parameters](includes/steps/prepare-parameters.md)]
- title: Convert
  durationInMinutes: 3
  content: |
    [!include[Content: convert](includes/steps/convert.md)]
```

## How to write a great tutorial

### ALLOW THE USER TO LEARN BY DOING​

In the beginning, we only learn anything by doing - it’s how we learn to talk, or walk.​

In your software tutorial, your learner needs to do things. The different things that they do while following your tutorial need to cover a wide range of tools and operations, building up from the simplest ones at the start to more complex ones.​

### GET THE USER STARTED​

It’s perfectly acceptable if your beginner’s first steps are hand-held baby steps. It’s also perfectly acceptable if what you get the beginner to do is not the way an experienced person would, or even if it’s not the ‘correct’ way - a tutorial for beginners is not the same thing as a manual for best practice.​

The point of a tutorial is to get your learner started on their journey, not to get them to a final destination.​

### MAKE SURE THE TUTORIAL WORKS​

One of your jobs as a tutor is to inspire the beginner’s confidence: in the software, in the tutorial, in the tutor and, of course, in their own ability to achieve what’s being asked of them.​

There are many things that contribute to this. A friendly tone helps, as does consistent use of language, and a logical progression through the material. But the single most important thing is that what you ask the beginner to do must work. The learner needs to see that the actions you ask them to take have the effect you say they will have.​

If the learner's actions produce an error or unexpected results, your tutorial has failed - even if it’s not your fault. When your students are there with you, you can rescue them; if they’re reading your documentation on their own you can’t - so you have to prevent that from happening in advance. This is without doubt easier said than done.​​

### ENSURE THE USER SEES RESULTS IMMEDIATELY​

Everything the learner does should accomplish something comprehensible, however small. If your student has to do strange and incomprehensible things for two pages before they even see a result, that’s much too long. The effect of every action should be visible and evident as soon as possible, and the connection to the action should be clear.​

The conclusion of each section of a tutorial, or the tutorial as a whole, must be a meaningful accomplishment.​

### MAKE YOUR TUTORIAL REPEATABLE​

Your tutorial must be reliably repeatable. This not easy to achieve: people will be coming to it with different operating systems, levels of experience and tools. What’s more, any software or resources they use are quite likely themselves to change in the meantime.​

The tutorial has to work for all of them, every time.​

Tutorials unfortunately need regular and detailed testing to make sure that they still work.​

### FOCUS ON CONCRETE STEPS, NOT ABSTRACT CONCEPTS​

Tutorials need to be concrete, built around specific, particular actions and outcomes.

The temptation to introduce abstraction is huge; it is after all how most computing derives its power. But all learning proceeds from the particular and concrete to the general and abstract, and asking the learner to appreciate levels of abstraction before they have even had a chance to grasp the concrete is poor teaching.​

### PROVIDE THE MINIMUM NECESSARY EXPLANATION​

Don’t explain anything the learner doesn’t need to know in order to complete the tutorial. Extended discussion is important - just not in a tutorial. In a tutorial, it is an obstruction and a distraction. Only the bare minimum is appropriate. Instead, link to explanations elsewhere in the documentation.​

### FOCUS ONLY ON THE STEPS THE USER NEEDS TO TAKE​

Your tutorial needs to be focused on the task in hand. Maybe the command you’re introducing has many other options, or maybe there are different ways to access a certain API. It doesn’t matter: right now, your learner does not need to know about those in order to make progress.​

#### Good luck and have fun teaching others!


<!-- Referenced links -->

[includes]: ./markdown-guide/index.md#included-markdown-files

<!-- referenced images -->

[overview]: media/how-to-create-tutorial-a-overview.png