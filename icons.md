---
uid: icon-naming-conventions
locale: en
title: Naming conventions for icons
description: Naming conventions for icons
so.topic: reference
so.date: 08.15.2022
so.author: Bergfrid Dias
---

# Icons

Icons are commonly reused in multiple files and thus stored as high in the [folder structure][1] as possible. Ideally in the repository's top-level *media/icons/* folder.

To create unique and consistent filenames that are also guessable and future proof we have adopted these best-practice conventions.

## Patterns

* English, lowercase, hyphenated
* Object-based (calendar)
* Primary object first (if no primary, use foreground)
* Shape before modifier
* Modifier as suffix (calendar-check)
* Arrows must have direction

For examples, see the list below.

## Variants of the same icon

| Attribute | Suffix | Example |
|---|---|---|
| Color | name of color | arrow-right-green |
| Filled | 'solid' | phone-solid |
| Size | 'large' if bigger than regular size | mailbox-large |

Don't use a serial number to distinguish variants of the same icon. Why? It makes it impossible to pick the right icon based on the filename. Instead, you'd have to open and preview the icon.

## Non-exhaustive list of icon names

### Arrows

**arrow:**

* arrow-down
  * arrow-down-a-z
  * arrow-down-arrow-up
  * arrow-down-from-line
  * arrow-down-left
  * arrow-down-right
* arrow-left
  * arrow-left-from-line
  * arrow-left-to-line
* arrow-pointer
* arrow-right
  * arrow-right-arrow-left
* arrow-up
  * arrow-up-from-bracket
  * arrow-up-left
  * arrow-up-right
    * arrow-up-right-from-square

**arrows:**

* arrows-maximize
* arrows-minimize
* arrows-repeat
* arrows-rotate
  * arrow-rotate-left
  * arrow-rotate-right
* arrows-spin
* arrow-trend
  * arrow-trend-down
  * arrow-trend-up
* arrows-to-dot

### Other, alphabetical

* address-book
* address-card
* apostrophe
* asterisk
* at
* ballot-check
* barcode
* bars
  * bars-filter
  * bars-sort
* bell
  * bell-plus
  * bell-exclamation
  * bell-slash
* book
* bookmark
* box
  * box-archive
  * box-open
* briefcase
* browser
* bug
* building
* bullhorn
* bullseye
  * bullseye-arrow
  * bullseye-pointer
* cabinet-filing
* call
  * call-start
  * call-stop
* calendar
  * calendar-check
  * calendar-circle-exclamation
  * calendar-circle-plus
* camera
* certificate
* chart
  * chart-line
    * chart-line-up
    * chart-line-down
  * chart-pie
* check
* chevron
  * chevrons-down
  * chevrons-left
  * chevrons-right
  * chevrons-up
* circle
  * circle-arrow-down
  * circle-envelope
  * circle-exclamation
  * circle-small
  * circle-xmark
* clapperboard
* clipboard
* clock
* clone
* cloud
  * cloud-arrow-download
* comment
  * comment-check
  * comment-dots
  * comment-exclamation
  * comment-lines
  * comment-question
  * comments
* compass
* copy
* copyright
* diamond-exclamation
* download
* envelope
  * envelope-circle-check
  * envelope-open
    * envelope-open-text
* file
  * file-arrow-down
  * file-lines
  * file-exclamation
  * file-export
  * file-import
* filter
* folder
  * folder-arrow-down
  * folder-arrow-up
  * folder-open
  * folder-plus
  * folder-tree
  * folders
* gears
* globe
* grid
* hand
* heart
  * heart-pulse
* hexagon
  * hexagon-exclamation
  * hexagon-stop
* hourglass
* inbox
  * inbox-in
  * inbox-out
* layer-group
* lightbulb
  * lightbulb-exclamation
* list
* location
  * location-arrow
* magnifying-glass
* mailbox
* message
  * message-exclamation
* microphone
* note-sticky
* notebook
* object
  * object-exclude
  * object-group
  * object-include
  * object-intersect
  * object-subtract
  * object-ungroup
  * object-union
* octagon-exclamation
* palette
* paperclip
* paste
* pause
* pen
* person
* phone
* plus-minus
* print
  * print-slash
* plus
* question
* recycle
* reply
  * reply-all
* rotate
  * rotate-left
  * rotate-right
* ruler
* shield
  * shield-check
  * shield-exclamation
* shuffle
* sidebar
* signal-stream
* sitemap
* sliders
* sort
  * sort-down
  * sort-up
* spell-check
* square
  * square-envelope
  * square-pen
  * square-xmark
* star
  * star-exclamation
* stop
* table
* tag
* thumbs-up
* ticket
* timer
* toggle
  * toggle-on
  * toggle-off
* trash-can
* triangle
  * triangle-exclamation
* video
  * video-solid
* user
  * user-group
* waveform

<!-- Referenced links-->
[1]: markdown-guide/index.md
