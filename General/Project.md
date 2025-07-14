---
related: 
tags: [project]
title: Project
description: 
status: 
people: 
project-type: 
deadline: 
product-feature: 
importance:
---

# Project

## Overview

## Goal

## Done Looks Like

## Teams & People

| Role                | Team Member | Responsibilities |
| ----------------------- | --------------- | -------------------- |
| Product Manager     |                 |                      |
| UX Designer         |                 |                      |
| UX Researcher       |                 |                      |
| Technical Lead      |                 |                      |
| Engineering         |                 |                      |
| Engineering Manager |                 |                      |
| Product Marketing   |                 |                      |
| Documentation       |                 |                      |

## Resources

## Notes

```dataview
TABLE dateformat(file.ctime, "yyyy-MM-dd") as "Created", dateformat(file.mtime, "yyyy-MM-dd") as "Updated"
FROM #note AND !#exclude AND !#archive
WHERE contains(project, this.file.name)
SORT file.ctime desc
```

## Meetings

```dataview
TABLE dateformat(file.ctime, "yyyy-MM-dd") as "Created", dateformat(file.mtime, "yyyy-MM-dd") as "Updated", file.folder as "Folder", people as "People"
FROM #meeting AND !#exclude AND !#archive
WHERE contains(project, this.file.name)
SORT file.ctime desc
```
