---
name: docs-maintainer
description: How to maintain and write good documentation files.
license: MIT
---

# Writing Documentation

## Before You Write

When tasked with documenting features, first look for a `docs` directory. Check whether existing documentation files cover the same topic and need updating. Enrich what is already there instead of starting from scratch. Update or remove outdated information. Only create new files when the topic is genuinely uncovered.

If `research` subagents are available, use them to gather additional information. When the topic is large and contains multiple sub-topics, create multiple files rather than one sprawling document.

## Writing Style

Documentation serves several purposes: discoverability of features and systems, understanding the general ideas behind a feature, learning how to use certain modules and abstractions, and knowing what to look for and where.

Documentation does not compete with code. Code is detailed; documentation guides the reader. From this, a few principles follow.

Be precise and technical, but avoid mirroring the code's level of detail. Include only the most impactful code snippets, one or two per file at most. Keep each file short but complete, covering exactly one topic. If a second topic is needed, create a separate file and cross-reference it.

Reference the most important files and directories by absolute path, but never dump a full directory tree. Describe the API shape conceptually: resource hierarchy, auth model, key operations. Do not enumerate every endpoint in a table, and do not list every field of every model. Link to the actual specification for the exhaustive list.

Write in flowing paragraphs with clear transitions between ideas. Vary sentence length: short sentences for emphasis, longer ones for explanation. Avoid template-like repetition, such as starting every sentence with the same verb. Do not use em dashes; use commas or parentheses instead.

Each documentation file should cover only one topic but may refer to related files.

## Structure Template

Split documentation files by topic, with each file named after the concept it documents. For example, a catalog feature would produce:

* `products.md`
* `categories.md`

Each file should be self-contained and answer exactly one question. Cross-reference between files where helpful.

A directory should contain at most eight files or subdirectories. When you exceed that limit, introduce a grouping subdirectory.

## Structure and Formatting

A document should be easy to skim. Use headings generously to group related content into visible sections. Use at least two heading levels: a top-level heading per file and second-level headings for each distinct topic.
A file has **AT LEAST** two second-level headings.
 
Mix formatting to keep the reader engaged:

* Paragraphs for explanation and narrative flow.
* Occasional bullet lists for the 3-5 things that naturally belong together.
* Occasional tables when comparing multiple items side by side. Keep tables under 10 rows.
* Bold or inline code for field names, key terms, and important values.

Avoid large monolithic paragraphs that run longer than 8-10 lines. If a paragraph covers more than one idea, split it or promote the sub-ideas to their own section.

Do not inline more than two file paths in a single paragraph. Group file references into a "Key Files" section or a bullet list instead.

## Common Pitfalls

- **Endpoint tables.** They are repetitive, go stale quickly, and duplicate the spec. Describe the resource shape instead.
- **Directory trees.** They rot faster than any other content. Name the most important files inline instead.
- **Mixed topics.** A file that covers API, database, architecture, and design decisions in sequence reads like a brain dump. Split it.
- **Field-by-field enumeration.** Listing every column of every table or every property of every model is tedious and unnecessary. Call out only the notable ones.
- **Identical sentence openings.** Starting four sentences in a row with "The" or "This" creates a choppy rhythm. Vary your openings.
- **Em dashes.** Never use them. Use commas or parentheses instead.
