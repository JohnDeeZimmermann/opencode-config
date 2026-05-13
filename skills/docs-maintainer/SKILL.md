---
name: docs-maintainer
description: How to maintain and write good documentation files.
license: MIT
---

# Writing Documentation

When tasked with documenting features, look for a `docs` directory.
First, look at what needs to be done: 

* Check whether there already are documentation files which cover the same topic that now need updating.
* Check whether previous docs can be enriched.
* Update and remove outdated information.
* Create new documentation files.

If `research` subagents are available, use these to gather additional information.

When what you are trying to cover is large and contains multiple sub-topics, create multiple files.

## Writing Documentation

You focus on making your texts simple to read. Documentation serves several purposes: 

* Discoverability of features and systems
* Understanding general ideas behind features
* How to use certain modules, systems and abstractions
* What to look for and where

Documentation tries to not compete with code: Code is detailed, documentation guides the reader. 
From that, several principles emerge when it comes to writing style: 

* Precise and technical but not overly detailed as that is what the actual code is for.
* Only give very few but impactful code snippet examples.
* Each documentation file should be short but as long as necessary.
* Simple and easy to reason about usage of headings.
* Reference only the most important files in the code. However, there is no need to map out the entire codebase.
* Reference other documentation files if applicable.
* Each file should cover only one topic but may refer to other related files instead.
* Sound as human as possible.
* Use bullet points sparringly. Prefer well-formatted sentences.

## Directory Structure

Group documentation files by module first, by topic second. 
Follow this simple rule of thumb: **Each directory should only contain at most eight files or other directories**.

Example: 

```
docs/
├── frontend/
│   ├── topic1/
│   │   ├── file1.md
│   │   ├── file2.md
│   │   └── ...
│   ├── topic2/
│   │   ├── file1.md
│   │   ├── file2.md
│   │   └── ...
│   └── ...
├── backend/
│   ├── topic1/
│   │   ├── file1.md
│   │   ├── file2.md
│   │   └── ...
│   ├── topic2/
│   │   ├── file1.md
│   │   ├── file2.md
│   │   └── ...
│   └── ...
└── ...
```
