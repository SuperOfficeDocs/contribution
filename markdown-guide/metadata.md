---
uid: markdown-metadata
locale: en
title: Metadata (Yaml front-matter)
description: 
so.topic: reference
so.date: 04.19.2021
so.author: Tony Yates
---

# Metadata (Yaml front-matter)

While you’re editing SuperOfficeDocs, you’ll see some lines at the very top of the document with things such as `uid`, `topic`, `locale`, and `title`. These items are referred to as **metadata** and use Yaml key-value front-matter syntax. They help the system properly create cross-referenced hyperlinks, related content links, and they help with language/edition filtering and sorting.

> [!NOTE]
> The section begins and ends with 3 dashes.

```yml
---
#Insert front matter here
---
```

## Example

```yml
---
uid: join_video_meeting
title: Join a video meeting
description: There are several ways in which you can join a video meeting in SuperOffice. Learn how.
author: Tony Yates
so.date: 04.19.2021
keywords: video
so.topic: howto
so.envir: cloud
so.client: online
---
```

## What to do

If you are editing a currently existing document, you won’t likely have to update much in the front matter section. Though, if you are creating a new document, please fill in as much as possible.

Before any updates get merged in the repo, the reviewers will check this section to make sure everything is good to go. One reason for reviewing this section is because the `uid` (unique identifier) must be, well… unique!
