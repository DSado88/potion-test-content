---
title: Document with Frontmatter
author: Test Author
date: 2026-02-17
tags:
  - testing
  - markdown
  - frontmatter
status: draft
priority: high
custom_field: "value with \"quotes\" and special chars: <>&"
---

# Document with YAML Frontmatter

This document has YAML frontmatter above. The renderer should either:
1. Display the frontmatter as metadata
2. Hide it and show only the body
3. Show it in a formatted properties table

## Body Content

The rest of this document is normal markdown content.

- Item one
- Item two
- Item three

> A blockquote for good measure.

```python
print("Hello from a frontmatter document!")
```
