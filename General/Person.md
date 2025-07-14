---
related: 
tags: [person]
title: Person
project: 
status: 
email: 
slack: 
birthday: 
importance: 
team: 
website: 
role: 
manager: 
department: 
location:
---

# Person

## Meetings

```dataview
LIST
FROM #meeting 
WHERE contains(people, "{{title}}")
SORT date DESC
LIMIT 10
```

## Projects

```dataview
LIST
FROM #project 
WHERE contains(people, "{{title}}")
SORT date DESC
```

## Notes

## Mentions

```dataview
LIST
FROM [[{{title}}]]
SORT file.mtime DESC
```
