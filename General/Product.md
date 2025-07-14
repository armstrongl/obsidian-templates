---
tags: [product]
related: 
title: Product
people: 
importance: 
project:
---

# Product

| Product  |     |
| -------- | --- |
| Release  |     |
| PM       |     |
| PMM      |     |
| Team     |     |
| Priority |     |

## Product Overview

### Core Concepts

### Key Features

### Use Cases

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

### Other People

```dataview
TABLE file.name as "Name", team as "Team", role as "Role", dateformat(file.mtime, "yyyy-MM-dd") as "Updated"
FROM #people AND [[]]
WHERE !contains(file.tags, "exclude") AND !contains(file.tags, "archive")
SORT file.ctime desc
```

## Resources

* Documentation topics:
	* Feature guide
	* Reference
	* Solution guides
	* Concepts
* Key code bases:
* Internal documents:
	* PRD
* External resources:
	* Blog post by XYZ

## Mentions

```dataview
TABLE dateformat(file.ctime, "yyyy-MM-dd") as "Created", dateformat(file.mtime, "yyyy-MM-dd") as "Updated", file.folder as "Folder"
WHERE contains(project, this.file.name) AND !contains(file.tags, "exclude") AND !contains(file.tags, "archive")
SORT file.ctime desc
```

## Technical Details

### Technical Architecture

#### Components

#### User Interfaces

### Limitations

## Market Fit

### Positioning and Messaging

### Customer Problems

### Competitive Positioning

### Pricing

### Important Customers
