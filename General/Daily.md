---
related:
aliases: ['<% tp.date.now("dddd, MMMM Do, YYYY") %>', <% tp.date.now("YYYY-MM-DD") %>]
tags: [daily]
title: '<% tp.date.now("dddd, MMMM Do, YYYY") %>'
title-alias: '<% tp.date.now("dddd, MMMM Do, YYYY") %>'
date: <% tp.date.now("YYYY-MM-DD") %>
week: <% tp.date.now("YYYY-MM-[W]ww") %>
---

# <% tp.date.now("dddd, MMMM Do, YYYY") %>

> [!RESOURCES] Key Resources
>
> - [[Journal/Weekly/<% tp.date.now("YYYY") %>/<% tp.date.now("MM MMMM") %>/Week <% tp.date.now("WW") %>|📅 Week <% tp.date.now("WW") %>]]

Today's focus (pick three):

## Log

## Notes

## Related

> [!DATAVIEW]- Created Today
>
> ```dataview
> List
> FROM ""
> WHERE striptime(file.cday) = striptime(date(today))
> AND !startswith(file.path, "_/")
> AND !contains(file.tags, "#exclude")
> SORT file.ctime DESC
> ```

> [!DATAVIEW]- Updated Today
>
> ```dataview
> List
> FROM ""
> WHERE striptime(file.mday) = striptime(date(today))
> AND !startswith(file.path, "_/")
> AND !contains(file.tags, "#exclude")
> SORT file.ctime DESC
> ```
