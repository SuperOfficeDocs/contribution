---
uid: markdown-guide-phosphor
title: Markdown guide for docs.superoffice.com
description: This Markdown style guide is intended to ensure that the markup of SuperOfficeDocs has a consistent style, and is easy to navigate and maintain.
keywords: Markdown, formatting, style guide
author: Bergfrid Dias, Tony Yates
date: 11.11.2024
topic: reference
language: en
---

<!-- markdownlint-disable-file MD044 -->

# Phosphor icons

The new SuperOffice UI uses [Phosphor font-based icons][8].

General format:

```markdown
<i class="ph ph-[icon-name]" aria-label="[Aria-label description]"></i>
```

Example:

```html
<i class="ph ph-star" aria-label="Star icon"></i>
```

## Usage guidelines

### In a header

* Place the icon **after the heading text**.
* Use `aria-label` and **include the word "icon"** to clarify its purpose (unless redundant).

```markdown
# Heading text <i class="ph ph-gear" aria-label="Gear icon"></i>
```

### Standalone in a table cell

* Place the icon **inside the table cell**.
* Use `aria-label` and **include the word "icon"**.

```markdown
| Icon | Feature |
|:-:|---|
| <i class="ph ph-gear" aria-label="Gear icon"></i> | Preferences |
```

### As a supplement to named UI components

* Place the icon **after the named UI component** in parentheses.
* Use `aria-hidden="true"` to prevent screen readers from redundantly announcing it (the text already provides the context).

```markdown
Click the **Preferences** button (<i class="ph ph-gear" aria-hidden="true"></i>) in the Navigator.
```

### Describing an action

* Use an **imperative phrase** with the icon.
* Use `aria-label` **without the word "icon"** to avoid unnecessary verbosity.

```markdown
Click <i class="ph ph-gear" aria-label="Gear"></i> to set your notification preferences.
```

### Decorative icons

If the icon is **purely decorative** and does not add meaningful information, use `aria-hidden="true"` to exclude it from the accessibility tree.

```markdown
<i class="ph ph-check" aria-hidden="true"></i>
```

## Reference

| Visual | Old path | Phosphor icon name | EN aria-label | Use case |
|:-:|---|---|---|---|
| <i class="ph ph-at" aria-label="Email icon"></i> | nav-inbox.png, pref-email.png | ph-at | Email icon | Inbox, email, email preferences, email document template |
| <i class="ph ph-basket" aria-label="Basket icon"></i> | nav-admin-appstore.png | ph-basket | Basket icon | App Store |
| <i class="ph ph-bell" aria-label="Bell icon"></i> | notice-new.png, pref-notification.png, diary-alarm.png | ph-bell | Bell icon | Notification |
| <i class="ph ph-calendar" aria-label="Diary icon"></i> | nav-diary.png | ph-calendar | Diary | Diary, Calendar |
| <i class="ph ph-calendar-blank" aria-label="Follow-up icon"></i> | appointment.png, appointment-followup.png, appointments-black.png | ph-calendar-blank | Follow-up, Meeting | Follow-up, Meeting |
| <i class="ph ph-calendar-check" aria-label="Task icon"></i> | task.png | ph-calendar-check | Task | Follow-up task |
| <i class="ph ph-chat-teardrop-text" aria-label="Chat bubble"></i> | chat.png, nav-admin-chat.png | ph-chat-teardrop-text | Chat bubble | Chat |
| <i class="ph ph-check" aria-label="Checkmark"></i> | check.png, check-black.png, diary-complete.png, btn-selected.png | ph-check | Checkmark/Check | Selected, Completed |
| <i class="ph ph-check-circle" aria-label="Check"></i> | pref-defaultvalues.png, select-all.png | ph-check-circle | Check | Default values |
| <i class="ph ph-clipboard-text" aria-label="Project icon"></i> | project.png, nav-project.png | ph-clipboard-text | Project icon | Project |
| <i class="ph ph-clock" aria-label="Clock icon"></i> | history.png, history-icon.png, nav-history.png, now.png | ph-clock | History, Clock icon | History, Time |
| <i class="ph ph-timer" aria-label="Timer icon"></i> | timespan.png | ph-timer | Timer icon | Timespan (requests) |
| <i class="ph ph-currency-circle-dollar" aria-label="Sale icon"></i> | nav-sale.png, pref-sale.png | ph-currency-circle-dollar | Sale icon | Sale |
| <i class="ph ph-gauge" aria-label="Dashboard icon"></i> | gauge.png, nav-dashboard.png | ph-gauge | Dashboard icon | Dashboard, Gauge chart |
| <i class="ph ph-gear" aria-label="Gear icon"></i> | cog-wheel.png, gearblack.png, pref-system.png, nav-admin-preferences.png | ph-gear | Gear icon | Settings, preferences |
| <i class="ph ph-list" aria-label="Main menu"></i> | menu-btn.png | ph-list | Main menu | Menu |
| <i class="ph ph-dots-three-circle-vertical" aria-label="Task menu"></i> | menu-btn.png | ph-dots-three-circle-vertical | Task menu | Menu |
| <i class="ph ph-list-bullets" aria-label="List icon"></i> | list.png, nav-admin-lists-active.png | ph-list-bullet | List icon | Lists |
| <i class="ph ph-text-columns" aria-label="Grouped lists icon"></i> |  | ph-text-columns | Grouped lists icon | Grouped lists |
| <i class="ph ph-list-plus" aria-label="Unpublished field"></i> | fields-unpublished-new.png  | ph-list-plus | Unpublished field| Custom objects |
| <i class="ph ph-sort-ascending" aria-label="Sort icon"></i> |  | ph-sort-ascending | Sort icon | Sorting |
| <i class="ph ph-sort-descending" aria-label="Sort icon"></i> |  | ph-sort-descending | Sort icon | Sorting |
| <i class="ph ph-rows" aria-label="Fields icon"></i> | nav-admin-fields.png | ph-rows | Fields icon | Fields |
| <i class="ph ph-sliders-horizontal" aria-label="Horizontal slider icon"></i> | nav-admin-options-active.png, options.png | ph-sliders-horizontal | Horizontal slider icon | Options|
| <i class="ph ph-barcode" aria-label="Barcode icon"></i> | nav-admin-products.png | ph-barcode | Barcode icon, Quote, Product | Quote, Product |
| <i class="ph ph-question" aria-label="Question mark"></i> | pref-learn-active.png, nav-admin-custcenter-active.png, diary-tentative.png | ph-question | Question mark | Customer Center |
| <i class="ph ph-shield" aria-label="Shield icon"></i> | nav-admin-privacy.png | ph-shield | Shield, Privacy icon, Visible for, Visible for group | Privacy, Visible for |
| <i class="ph ph-shield-check" aria-label="Shield icon"></i> |  | ph-shield-check | Shield icon, Visible for me | Visible for |
| <i class="ph ph-shield-slash" aria-label="Shield icon"></i> |  | ph-shield-slash | Shield icon, Visible for all | Visible for |
| <i class="ph ph-sidebar-simple" aria-label="Sidebar icon"></i> | left-collapse.png, left-expand.png, right-collapse.png | ph-sidebar-simple | Sidebar icon | Expand/collapse navigator, Show/hide preview |
| <i class="ph ph-subtract-square" aria-label="Selection icon"></i> | nav-selection.png | ph-subtract-square | Selection icon | Selection |
| <i class="ph ph-magnifying-glass" aria-label="Search icon"></i> | search-icon-black.png, nav-search.png | ph-magnifying-glass | Search icon | Search |
| <i class="ph ph-list-magnifying-glass" aria-label="Find icon"></i> |  | ph-list-magnifying-glass | Find icon | Find |
| <i class="ph ph-magic-wand" aria-label="Visual effects"></i> |  | ph-magic-wand | Visual effects | UI |
| <i class="ph ph-sparkle" aria-label="Sparkle icon"></i> |  | ph-sparkle | Sparkle icon, AI | AI services |
| <i class="ph ph-star" aria-label="Star icon"></i> | favourite-no.png, favourite-yes.png, nav-fav.png | ph-star | Star icon, Favorites | Favorites |
| <i class="ph ph-ticket" aria-label="Request icon"></i> | ticket.png, ticket-home.png, pref-request.png, nav-admin-requests-active.png, nav-cs.png | ph-ticket | Ticket, Request icon | Request, Service |
| <i class="ph ph-target" aria-label="Marketing icon"></i> | mailings.png, marketing.png, nav-marketing.png | ph-target | Marketing icon | Marketing |
| <i class="ph ph-buildings" aria-label="Company icon"></i> | nav-company.png, company.png | ph-buildings | Company icon | Company (card) |
| <i class="ph ph-user" aria-label="User icon"></i> | nav-admin-users-active.png | ph-user | Single user icon | User management |
| <i class="ph ph-user-circle" aria-label="Contact icon"></i> | person.png, contact.png, nav-contact.png, pref-person.png, personal-settings.png | ph-user-circle | Contact icon, Personal settings | Contact card, Person, User profile |
| <i class="ph ph-users" aria-label="Relations icon"></i> | | ph-users | Relations icon | Relations |
| <i class="ph ph-users-three" aria-label="User icon"></i> | | ph-users-three | Three users icon | |
| <i class="ph ph-wrench" aria-label="Tool icon"></i> | nav-tools.png, settingstools.png | ph-wrench | Tool icon | Access to external applications |
| <i class="ph ph-x" aria-label="Remove icon"></i> | remove-icon.png, red-x.png, delete.png, window-close.ong, reject-appointment-icon.png | ph-x | Remove icon (or simply 'X') | Remove, X, Close dialog |
| <i class="ph ph-x-circle" aria-label="Remove icon"></i> | delete-circle-red.png | ph-x-circle | Remove icon (or simply 'X') | Same as ph-x |
| <i class="ph ph-globe" aria-label="Web services icon"></i> | show-url.png | ph-globe | Globe icon, Web services | Web services |
| <i class="ph ph-globe-hemisphere-east" aria-label="Remove icon"></i> |  | ph-globe-hemisphere-east | Web panels icon (or simply 'Globe') | Web panels |
| <i class="ph ph-arrows-left-right" aria-label="Workflow icon"></i> | nav-admin-workflow-active.png  | ph-arrows-left-right | Workflow icon | Workflow |
| <i class="ph ph-traffic-signal" aria-label="Role icon"></i> | nav-admin-roles-active.png | ph-traffic-signal | Role icon | Roles |
| <i class="ph ph-file-arrow-up" aria-label="Import icon"></i> | nav-admin-import-active.png | ph-file-arrow-up | Import icon | Import |
| <i class="ph ph-code-block" aria-label="Script icon"></i> | nav-admin-crmscript-active.png | ph-code-block | Script icon | CRMScript |
| <i class="ph ph-lock-simple" aria-label="Padlock icon"></i> | nav-admin-licenses-active.png, lock.on.png | ph-lock-simple | Padlock icon | Licenses, Lock/unlock sales target |
| <i class="ph ph-lock-simple-open" aria-label="Open padlock icon"></i> | lock-off.png | ph-lock-simple-open | Open padlock icon | Lock/unlock sales target |
| <i class="ph ph-squares-four" aria-label="Screen designer"></i> | nav-admin-confscreen-active.png | ph-squares-four | Screen designer icon | Screen designer |
| <i class="ph ph-selection-all" aria-label="System design"></i> | nav-admin-systemdesign-active.png | ph-selection-all | System design icon | System design |
| <i class="ph ph-chart-bar" aria-label="SAINT"></i> | bar.png, column-bar.png, nav-admin-saint-active.png | ph-chart-bar | SAINT icon, chart | SAINT, Dashboards |
| <i class="ph ph-chart-pie" aria-label="Pie chart"></i> | pie.png | ph-chart-pie | Pie chart | Dashboards |
| <i class="ph ph-number-square-three" aria-label="Big numbers"></i> | big-numbers.png | ph-number-square-three | Chart | Dashboards |
| <i class="ph ph-chart-line-up" aria-label="Line chart"></i> | line.png | ph-chart-line | Chart | Dashboards |
| <i class="ph ph-funnel" aria-label="Filter icon"></i> | filter-icon.png, filter-column.png | ph-funnel | Filter icon | Filter |
| <i class="ph ph-caret-down" aria-label="Chevron"></i> | dropdown-icon.png, dropdown-arrow.png, arrow-down.png | ph-caret-down | Chevron | Chevron on drop-down list |
| <i class="ph ph-caret-right" aria-label="Chevron"></i> | menu-arrow.png | ph-caret-right | Chevron | Expand sub list |
| <i class="ph ph-arrow-clockwise" aria-label="Refresh"></i> | refresh.png, refresh-icon.png, diary-recurring.png | ph-arrow-clockwise | Refresh | Refresh, Reload, Repeat |
| <i class="ph ph-arrow-bend-up-left" aria-label="Reply"></i> | reply-icon.png | ph-arrow-bend-up-left | Reply | Reply |
| <i class="ph ph-arrow-bend-double-up-left" aria-label="Reply all"></i> | reply-all-icon.png | ph-arrow-bend-double-up-left | Reply all | Reply all |
| <i class="ph ph-arrow-bend-up-right" aria-label="Forward"></i> | forward-icon.png | ph-arrow-bend-up-right | Forward | Forward |
| <i class="ph ph-warning" aria-label="Warning icon"></i> | warning.png, warning-red.png | ph-warning | Warning icon | Warning, alert |
| <i class="ph ph-warning-circle" aria-label="Warning icon"></i> | exclamation.png, mandatory.png, ops.png | ph-warning-circle | Warning icon | Call out |
| <i class="ph ph-archive" aria-label="Archive icon"></i> | archive-icon.png | ph-archive | Archive icon | Archive (email) |
| <i class="ph ph-paperclip" aria-label="Attachment icon"></i> | attachments-black.png, attachments-theme.png | ph-paperclip | Attachment icon, Attachments | Attachments |
| <i class="ph ph-dots-three" aria-label="Three dots"></i> | addcomment.png | ph-dots-three | Three dots | Comment on request |
| <i class="ph ph-info" aria-label="Info"></i> | info-ball.png | ph-info | Info icon | Tooltip |
| <i class="ph ph-folder" aria-label="Folder icon"></i> | folder.png | ph-folder | Folder icon | Folder |
| <i class="ph ph-flag" aria-label="Flag icon"></i> | flag-on.png, flag-off.png | ph-flag | Flag icon | Flag messages |
| <i class="ph ph-pencil-simple" aria-label="Edit icon"></i> | edit.png, edit-black.png | ph-pencil-simple | Edit icon | Edit |
| <i class="ph ph-note-pencil" aria-label="Edit icon"></i> | edit-pen.png | ph-note-pencil | Edit icon | Edit tile (in dashboard) |
| <i class="ph ph-push-pin" aria-label="Pin"></i> |  | ph-push-pin | Pin | Pin |
| <i class="ph ph-bug" aria-label="Bug"></i> | bug.png | ph-bug | Bug | Bug, Troubleshooting |
| <i class="ph ph-copy" aria-label="Copy"></i> | duplicate-icon.png, diary-copy.png | ph-copy | Copy | Copy, Duplicate |
| <i class="ph ph-video-camera" aria-label="Video meeting"></i> | videocall.png, videocall-off.png, diary-videocall.png, videomeeting_inactive.png, videomeeting_active.png, videomeeting_diaryicon.png | ph-video-camera | Video meeting | Video meeting, Video call |
| <i class="ph ph-phone" aria-label="Phone"></i> | phone.png | ph-phone | Phone call | Phone call |
| <i class="ph ph-file-doc" aria-label="Document"></i> | document.png | ph-file-doc | Document | Document |
| <i class="ph ph-files" aria-label="Templates"></i> | document.png | ph-files | Templates | Document templates |
| <i class="ph ph-arrow-square-out" aria-label="New window"></i> | new-window-icon.png | ph-arrow-square-out | New window, External link  | |
| <i class="ph ph-smiley" aria-label="Smiley"></i> | smiley-icon.png, sentiment-positive.png | ph-smiley | Smiley, Positive  | Emoji |
| <i class="ph ph-smiley-sad" aria-label="Smiley"></i> | sentiment-negative.png | ph-smiley-sad | Smiley, Negative  | Emoji |
| <i class="ph ph-smiley-meh" aria-label="Smiley"></i> | sentiment-neutral.png | ph-smiley-meh | Smiley, Neutral  | Emoji |
| <i class="ph ph-toggle-right" aria-label="Functions"></i> | pref-function.png | ph-toggle-right | Functions, Toggle icon  | Functions |
| <i class="ph ph-plus" aria-label="Add"></i> | add-field.png | ph-plus | Add, Plus  | Add |
| <i class="ph ph-minus-circle" aria-label="Unselect all"></i> | unselect-all.png | ph-minus-circle | Unselect | |
| <i class="ph ph-equals" aria-label="Move"></i> | criteria-move.png | ph-equals | Move, =  | Find screen |
| <i class="ph ph-text-a-underline" aria-label="Show/hide toolbar"></i> | format-font.png, msg-toolbar.png | ph-text-a-underline | Show/hide toolbar | show or hide the toolbar in the message editor |
| <i class="ph ph-arrow-circle-up" aria-label="Arrow up"></i> | arrow-up.png | ph-arrow-circle-up | Arrow up | Direction |
| <i class="ph ph-arrow-circle-down" aria-label="Arrow down"></i> | arrow-down.png | ph-arrow-circle-down | Arrow down | Direction |
| <i class="ph ph-arrow-circle-left" aria-label="Arrow left"></i> | arrow-left.png | ph-arrow-circle-left | Arrow left | Direction |
| <i class="ph ph-arrow-circle-right" aria-label="Arrow right"></i> | arrow-right.png | ph-arrow-circle-right | Arrow right | Direction |
| <i class="ph ph-arrow-left" aria-label="Arrow left"></i> | arrow-left.png | ph-arrow-left | Arrow left | Pagination |
| <i class="ph ph-arrow-right" aria-label="Arrow right"></i> | arrow-right.png | ph-arrow-right | Arrow right | Pagination |
| <i class="ph ph-text-align-left" aria-label="Align left"></i> | align-left.png, title.png | ph-text-align-left | Align left | Justifying text |
| <i class="ph ph-text-align-right" aria-label="Align right"></i> | align-right.png | ph-text-align-right | Align right | Justifying text |
| <i class="ph ph-eye" aria-label="Eye"></i> | visibility.png | ph-eye | Eye | Visibility, See |
| <i class="ph ph-split-horizontal" aria-label="Resize"></i> | resize-horizontal.png | ph-split-horizontal | | GUI |
| <i class="ph ph-split-vertical" aria-label="Resize"></i> | resize-vertical.png | ph-split-vertical | | GUI |
| <i class="ph ph-download-simple" aria-label="Download"></i> | export.png | ph-download-simple | Download | Export, Download |
| <i class="ph ph-diamond" aria-label="Milestone"></i> | milestone-icon.png | ph-diamond | Milestone | Projects |
| <i class="ph ph-device-mobile" aria-label="Mobile icon"></i> | mobile.png | ph-device-mobile | Mobile icon | Responsive design |
| <i class="ph ph-monitor" aria-label="Desktop"></i> | desktop.png | ph-monitor | Desktop | Responsive design |
| <i class="ph ph-monitor" aria-label="Chart"></i> | desktop.png | ph-monitor | Chart | Dashboard |

## Translated labels

| Phosphor icon name | DA (Danish)| DE (German) | NO (Norwegian)| NL (Dutch)| SV (Swedish) |
|:-:|---|---|---|---|---|
| ph-gear | Tandhjulsikon | Zahnrad-Symbol | Gear-ikon | Tandwielpictogram | Kugghjulsikon |

## Legacy icons still in use

| Visual | Path | Use case |
|:-:|---|---|
| ![icon][img1] | common/icons/copy-paste-icon.png | Requests |
| ![icon][img2] | media/icons/admin/import-outlook-small.png | Import |
| ![icon][img3] | media/icons/admin/import-erp-small.png | Import |
| ![icon][img4] | media/icons/admin/import-gmail-small.png | Import |
| ![icon][img5] | media/icons/admin/import-erp-small.png | Import |
| ![icon][img6] | media/icons/admin/import-preview-icon-product-new.png | Import |
| ![icon][img7] | media/icons/admin/import-preview-icon-product-changed.png | Import |
| ![icon][img8] | media/icons/admin/import-preview-icon-person-new.png | Import |
| ![icon][img9] | media/icons/admin/import-preview-icon-person-changed.png | Import |
| ![icon][img10] | media/icons/admin/import-preview-icon-company-new.png | Import |
| ![icon][img11] | media/icons/mail-link/add-document.png | MailLink |
| ![icon][img12] | media/icons/mail-link/arrow.png | MailLink |
| ![icon][img13] | media/icons/mail-link/archive-to-superoffice-crm.png | MailLink |
| ![icon][img14] | media/icons/mail-link/search-for-sender-in-superoffice-crm.png | MailLink |
| ![icon][img15] | media/icons/mail-link/add-recipient.png | MailLink |
| ![icon][img16] | media/icons/mail-link/archive-is-on.png | MailLink |
| ![icon][img17] | media/icons/mail-link/archive-is-off.png | MailLink |
| ![icon][img18] | media/icons/mail-link/already-archived.png | MailLink |
| ![icon][img19] | media/icons/gmail-link/btn-archive-more.png | GmailLink |
| ![icon][img20] | media/icons/gmail-link/btn-archive-attachment.png | GmailLink |
| ![icon][img21] | media/icons/marketing-and-forms/side-panel-content.png | Marketing |
| ![icon][img22] | media/icons/marketing-and-forms/side-panel-content-columns.png | Marketing |
| ![icon][img23] | media/icons/marketing-and-forms/side-panel-content-button.png | Marketing |
| ![icon][img24] | media/icons/marketing-and-forms/side-panel-content-divider.png | Marketing |
| ![icon][img25] | media/icons/marketing-and-forms/side-panel-content-heading.png | Marketing |
| ![icon][img26] | media/icons/marketing-and-forms/side-panel-content-html.png | Marketing |
| ![icon][img27] | media/icons/marketing-and-forms/side-panel-content-image.png | Marketing |
| ![icon][img28] | media/icons/marketing-and-forms/side-panel-content-menu.png | Marketing |
| ![icon][img29] | media/icons/marketing-and-forms/side-panel-content-social.png | Marketing |
| ![icon][img30] | media/icons/marketing-and-forms/side-panel-content-text.png | Marketing |
| ![icon][img31] | media/icons/marketing-and-forms/side-panel-content-receipt.png | Marketing |
| ![icon][img32] | media/icons/marketing-and-forms/side-panel-blocks.png | Marketing |
| ![icon][img33] | media/icons/marketing-and-forms/save-block.png | Marketing |
| ![icon][img34] | media/icons/marketing-and-forms/side-panel-body.png | Marketing |
| ![icon][img35] | media/icons/marketing-and-forms/add-row.png | Marketing |
| ![icon][img36] | media/icons/marketing-and-forms/move-2.png | Marketing |
| ![icon][img39] | media/icons/marketing-and-forms/move-field.png | Marketing |
| ![icon][img37] | media/icons/marketing-and-forms/cancel.png | Marketing |
| ![icon][img38] | media/icons/marketing-and-forms/copy.jpg | Marketing |
| ![icon][img40] | media/icons/marketing-and-forms/undo-redo.png | Marketing |
| ![icon][img41] | media/icons/marketing-and-forms/side-panel-images.png | Marketing |
| ![icon][img42] | media/icons/marketing-and-forms/side-panel-audit.png | Marketing |
| ![icon][img43] | media/icons/marketing-and-forms/side-panel-images-small.png | Marketing |
| ![icon][img44] | media/icons/marketing-and-forms/side-panel-content-small.png | Marketing |
| ![icon][img45] | media/icons/marketing-and-forms/form-active.png | Marketing |
| ![icon][img46] | media/icons/marketing-and-forms/edit.png | Marketing |
| ![icon][img47] | media/icons/sign-editor-variables.png | Template variables |
| ![icon][img48] | media/icons/document-lock-editing.png | Old document dialog |
| ![icon][img49] | media/icons/document-lock-locked.png | Old document dialog |
| ![icon][img51] | media/icons/quote-state-draft.png | Quote |
| ![icon][img52] | media/icons/quote-state-draft-not-calculated.png | Quote |
| ![icon][img53] | media/icons/quote-state-needs-approval.png | Quote |
| ![icon][img54] | media/icons/quote-state-approved.png | Quote |
| ![icon][img55] | media/icons/quote-state-not-approved.png | Quote |
| ![icon][img56] | media/icons/quote-state-published.png | Quote |
| ![icon][img57] | media/icons/quote-state-published-expired.png | Quote |
| ![icon][img58] | media/icons/quote-state-sold.png | Quote |
| ![icon][img59] | media/icons/quote-state-rejected.png | Quote |
| ![icon][img60] | media/icons/quote-state-ordered.png | Quote |
| ![icon][img61] | media/icons/quote-state-archived.png | Quote |
| ![icon][img62] | media/icons/quote-status-ok.png | Quote |
| ![icon][img63] | media/icons/quote-status-ok-with-info.png | Quote |
| ![icon][img64] | media/icons/quote-status-error.png | Quote |
| ![icon][img65] | media/icons/admin/sync-none.png | Quote |
| ![icon][img66] | media/icons/admin/sync-2-way.png | Quote |
| ![icon][img67] | media/icons/admin/sync-to-erp.png | Quote |
| ![icon][img68] | media/icons/admin/sync-to-so.png | Quote |
| ![icon][img69] | media/icons/admin/sync-deactivated.png | Quote |
| ![icon][img70] | common/icons/view-list.png | Flows |
| ![icon][img71] | common/icons/view-thumbs.png | Flows |
| | common/icons/selection-combined*.png | Selections|
| ![icon][img72] | common/icons/area.png | Dashboards |
| ![icon][img73] | common/icons/combined.png | Dashboards |
| ![icon][img74] | common/icons/combined-bar.png | Dashboards |

## Accessibility tips

* Use `aria-label` for all functional icons to ensure they are announced correctly by screen readers.
* Keep `aria-label`s concise and directly descriptive.
* Use `aria-hidden="true"` for decorative icons to reduce noise for screen reader users.
* Test your content with a screen reader to verify clarity and usability.

<!-- Referenced links -->
[8]: https://phosphoricons.com/

<!-- Referenced images -->
[img1]: ../../superoffice-docs/common/icons/copy-paste-icon.png
[img2]: ../../superoffice-docs/docs/media/icons/admin/import-outlook-small.png
[img3]: ../../superoffice-docs/docs/media/icons/admin/import-erp-small.png
[img4]: ../../superoffice-docs/docs/media/icons/admin/import-gmail-small.png
[img5]: ../../superoffice-docs/docs/media/icons/admin/import-erp-small.png
[img6]: ../../superoffice-docs/docs/media/icons/admin/import-preview-icon-product-new.png
[img7]: ../../superoffice-docs/docs/media/icons/admin/import-preview-icon-product-changed.png
[img8]: ../../superoffice-docs/docs/media/icons/admin/import-preview-icon-person-new.png
[img9]: ../../superoffice-docs/docs/media/icons/admin/import-preview-icon-person-changed.png
[img10]: ../../superoffice-docs/docs/media/icons/admin/import-preview-icon-company-new.png
[img11]: ../../superoffice-docs/docs/media/icons/mail-link/add-document.png
[img12]: ../../superoffice-docs/docs/media/icons/mail-link/arrow.png
[img13]: ../../superoffice-docs/docs/media/icons/mail-link/archive-to-superoffice-crm.png
[img14]: ../../superoffice-docs/docs/media/icons/mail-link/search-for-sender-in-superoffice-crm.png
[img15]: ../../superoffice-docs/docs/media/icons/mail-link/add-recipient.png
[img16]: ../../superoffice-docs/docs/media/icons/mail-link/archive-is-on.png
[img17]: ../../superoffice-docs/docs/media/icons/mail-link/archive-is-off.png
[img18]: ../../superoffice-docs/docs/media/icons/mail-link/already-archived.png
[img19]: ../../superoffice-docs/docs/media/icons/gmail-link/btn-archive-more.png
[img20]: ../../superoffice-docs/docs/media/icons/gmail-link/btn-archive-attachment.png
[img21]: ../../superoffice-docs/docs/media/icons/marketing-and-forms/side-panel-content.png
[img44]: ../../superoffice-docs/docs/media/icons/marketing-and-forms/side-panel-content-small.png
[img22]: ../../superoffice-docs/docs/media/icons/marketing-and-forms/side-panel-content-columns.png
[img23]: ../../superoffice-docs/docs/media/icons/marketing-and-forms/side-panel-content-button.png
[img24]: ../../superoffice-docs/docs/media/icons/marketing-and-forms/side-panel-content-divider.png
[img25]: ../../superoffice-docs/docs/media/icons/marketing-and-forms/side-panel-content-heading.png
[img26]: ../../superoffice-docs/docs/media/icons/marketing-and-forms/side-panel-content-html.png
[img27]: ../../superoffice-docs/docs/media/icons/marketing-and-forms/side-panel-content-image.png
[img28]: ../../superoffice-docs/docs/media/icons/marketing-and-forms/side-panel-content-menu.png
[img29]: ../../superoffice-docs/docs/media/icons/marketing-and-forms/side-panel-content-social.png
[img30]: ../../superoffice-docs/docs/media/icons/marketing-and-forms/side-panel-content-text.png
[img31]: ../../superoffice-docs/docs/media/icons/marketing-and-forms/side-panel-content-receipt.png
[img32]: ../../superoffice-docs/docs/media/icons/marketing-and-forms/side-panel-blocks.png
[img41]: ../../superoffice-docs/docs/media/icons/marketing-and-forms/side-panel-images.png
[img43]: ../../superoffice-docs/docs/media/icons/marketing-and-forms/side-panel-images-small.png
[img42]: ../../superoffice-docs/docs/media/icons/marketing-and-forms/side-panel-audit.png
[img33]: ../../superoffice-docs/docs/media/icons/marketing-and-forms/save-block.png
[img34]: ../../superoffice-docs/docs/media/icons/marketing-and-forms/side-panel-body.png
[img35]: ../../superoffice-docs/docs/media/icons/marketing-and-forms/add-row.png
[img36]: ../../superoffice-docs/docs/media/icons/marketing-and-forms/move-2.png
[img37]: ../../superoffice-docs/docs/media/icons/marketing-and-forms/cancel.png
[img38]: ../../superoffice-docs/docs/media/icons/marketing-and-forms/copy.jpg
[img39]: ../../superoffice-docs/docs/media/icons/marketing-and-forms/move-field.png
[img40]: ../../superoffice-docs/docs/media/icons/marketing-and-forms/undo-redo.png
[img45]: ../../superoffice-docs/docs/media/icons/marketing-and-forms/form-active.png
[img46]: ../../superoffice-docs/docs/media/icons/marketing-and-forms/edit.png
[img47]: ../../superoffice-docs/docs/media/icons/sign-editor-variables.png
[img48]: ../../superoffice-docs/docs/media/icons/document-lock-editing.png
[img49]: ../../superoffice-docs/docs/media/icons/document-lock-locked.png
[img51]: ../../superoffice-docs/docs/media/icons/quote-state-draft.png
[img52]: ../../superoffice-docs/docs/media/icons/quote-state-draft-not-calculated.png
[img53]: ../../superoffice-docs/docs/media/icons/quote-state-needs-approval.png
[img54]: ../../superoffice-docs/docs/media/icons/quote-state-approved.png
[img55]: ../../superoffice-docs/docs/media/icons/quote-state-not-approved.png
[img56]: ../../superoffice-docs/docs/media/icons/quote-state-published.png
[img57]: ../../superoffice-docs/docs/media/icons/quote-state-published-expired.png
[img58]: ../../superoffice-docs/docs/media/icons/quote-state-sold.png
[img59]: ../../superoffice-docs/docs/media/icons/quote-state-rejected.png
[img60]: ../../superoffice-docs/docs/media/icons/quote-state-ordered.png
[img61]: ../../superoffice-docs/docs/media/icons/quote-state-archived.png
[img62]: ../../superoffice-docs/docs/media/icons/quote-status-ok.png
[img63]: ../../superoffice-docs/docs/media/icons/quote-status-ok-with-info.png
[img64]: ../../superoffice-docs/docs/media/icons/quote-status-error.png
[img65]: ../../superoffice-docs/docs/media/icons/admin/sync-none.png
[img66]: ../../superoffice-docs/docs/media/icons/admin/sync-2-way.png
[img67]: ../../superoffice-docs/docs/media/icons/admin/sync-to-erp.png
[img68]: ../../superoffice-docs/docs/media/icons/admin/sync-to-so.png
[img69]: ../../superoffice-docs/docs/media/icons/admin/sync-deactivated.png
[img70]: ../../superoffice-docs/common/icons/view-list.png
[img71]: ../../superoffice-docs/common/icons/view-thumbs.png
[img72]: ../../superoffice-docs/common/icons/area.png
[img73]: ../../superoffice-docs/common/icons/combined.png
[img74]: ../../superoffice-docs/common/icons/combined-bar.png
