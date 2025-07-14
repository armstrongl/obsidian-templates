---
aliases: ["Week <% tp.date.now('WW') %> of <% tp.date.now('YYYY') %>"]
related:
tags: [weekly]
title: "Week <% tp.date.now('WW') %> of <% tp.date.now('YYYY') %>"
date: <% tp.date.now("YYYY-MM-DD") %>
week: <% tp.date.now("YYYY-MM-[W]ww") %>
title-alias: "Week <% tp.date.now('WW') %> of <% tp.date.now('YYYY') %>"
---

# Week <% tp.date.now('WW') %> of <% tp.date.now('YYYY') %>

_Week of <% tp.date.now("MMMM Do") %> - <% moment().add(6, 'days').format("MMMM Do") %>_

> [!RESOURCES] Key Resources
>
> - Example Resource

## Weekly Objectives

_Set 3-5 strategic goals that align with larger initiatives._

_What would success look like this week?_

## Overview

### [[Journal/Daily/<% moment().startOf('week').add(1, 'days').format("YYYY") %>/<% moment().startOf('week').add(1, 'days').format("MM MMMM") %>/<% moment().startOf('week').add(1, 'days').format("DD dddd") %>|Monday <% moment().startOf('week').add(1, 'days').format("MMMM Do") %>]]

**Planned:**
**Achieved:**
**Blockers:**

### [[Journal/Daily/<% moment().startOf('week').add(2, 'days').format("YYYY") %>/<% moment().startOf('week').add(2, 'days').format("MM MMMM") %>/<% moment().startOf('week').add(2, 'days').format("DD dddd") %>|Tuesday <% moment().startOf('week').add(2, 'days').format("MMMM Do") %>]]

**Planned:**
**Achieved:**
**Blockers:**

### [[Journal/Daily/<% moment().startOf('week').add(3, 'days').format("YYYY") %>/<% moment().startOf('week').add(3, 'days').format("MM MMMM") %>/<% moment().startOf('week').add(3, 'days').format("DD dddd") %>|Wednesday <% moment().startOf('week').add(3, 'days').format("MMMM Do") %>]]

**Planned:**
**Achieved:**
**Blockers:**

### [[Journal/Daily/<% moment().startOf('week').add(4, 'days').format("YYYY") %>/<% moment().startOf('week').add(4, 'days').format("MM MMMM") %>/<% moment().startOf('week').add(4, 'days').format("DD dddd") %>|Thursday <% moment().startOf('week').add(4, 'days').format("MMMM Do") %>]]

**Planned:**
**Achieved:**
**Blockers:**

### [[Journal/Daily/<% moment().startOf('week').add(5, 'days').format("YYYY") %>/<% moment().startOf('week').add(5, 'days').format("MM MMMM") %>/<% moment().startOf('week').add(45, 'days').format("DD dddd") %>|Friday <% moment().startOf('week').add(5, 'days').format("MMMM Do") %>]]

**Planned:**
**Achieved:**
**Blockers:**

## Meetings

- **Monday**:
 	- None
- **Tuesday**:
 	- Some Meeting | [NOTES](https://example.com) | 12:00 PM → 1:30 PM
- **Wednesday**:
 	- None
- **Thursday**:
 	- Some Meeting | [NOTES](https://example.com) | 3:15 PM → 4:15 PM
- **Friday**:
 	- Some Meeting | [NOTES](https://example.com) | 11:00 AM → 11:30 AM
- **Others**:
 	- Company All-Hands

## Stakeholder Touchpoints & Project Progress

> [!TODO] Project Status Updates
>
> ```dataview
> TABLE WITHOUT ID
> choice(status = "Ongoing", "🟢", choice(status = "In Progress", "🔵", choice(status = "Planned", "⚪", choice(status = "On Hold", "🟡", choice(status = "Complete", "✅", "🔴"))))) as Status,
> file.link as Project,
> project-type as "Project Type",
> dateformat(file.mtime, "MMM dd") as "Last Updated"
> FROM "Resources/Projects"
> WHERE status != "Complete"
> SORT status DESC, file.mtime DESC
> ```

## Other Files

> [!DATAVIEW]- Created This Week
>
> ```dataview
> TABLE rows.file.name AS "File Name", rows.file.folder AS "Folder"
> FROM ""
> WHERE striptime(file.cday) >= striptime(date(today)) - dur(6 days)
> AND striptime(file.cday) <= striptime(date(today))
> AND !startswith(file.path, "_/")
> AND !contains(file.tags, "#exclude")
> GROUP BY dateformat(file.cday, "cccc MMMM dd") AS "Day"
> SORT rows.file.cday[0] ASC
> ```

> [!DATAVIEW]- Updated This Week
>
> ```dataview
> TABLE rows.file.name AS "File Name", rows.file.folder AS "Folder"
> FROM ""
> WHERE striptime(file.mday) >= striptime(date(today)) - dur(6 days)
> AND striptime(file.mday) <= striptime(date(today))
> AND !startswith(file.path, "_/")
> AND !contains(file.tags, "#exclude")
> GROUP BY dateformat(file.mday, "cccc MMMM dd") AS "Day"
> SORT rows.file.mday[0] ASC
> ```
