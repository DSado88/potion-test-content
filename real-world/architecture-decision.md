# ADR-001: Use Plate.js for Rich Text Editing

**Status:** Accepted
**Date:** 2026-01-20
**Deciders:** Alice, Bob, Carol

## Context

We need a rich text editor for the document browser. The editor must support:

- Markdown-like editing experience
- Real-time collaboration (future)
- Custom block types (callouts, toggles, databases)
- Slash commands
- Inline formatting toolbar

## Considered Options

### 1. Plate.js (based on Slate)

**Pros:**
- Highly extensible plugin architecture
- Active community and development
- TypeScript-first
- Supports collaborative editing via Yjs
- Large ecosystem of pre-built plugins

**Cons:**
- Steep learning curve
- Documentation can be sparse
- Breaking changes between major versions
- Bundle size (~200KB gzipped with plugins)

### 2. TipTap (based on ProseMirror)

**Pros:**
- Excellent documentation
- Simpler API for common use cases
- Good collaborative editing support
- Smaller community but very responsive maintainers

**Cons:**
- Less flexible for custom block types
- ProseMirror schema can be restrictive
- Fewer pre-built extensions than Plate.js

### 3. Lexical (by Meta)

**Pros:**
- Excellent performance
- Small bundle size
- Backed by Meta
- Good accessibility out of the box

**Cons:**
- Younger ecosystem, fewer plugins
- More low-level, requires more custom code
- Collaborative editing is still experimental

## Decision

We chose **Plate.js** because:

1. The plugin architecture aligns with our need for custom blocks
2. Slate's data model (JSON tree) maps naturally to our markdown ↔ rich text conversion
3. The `@platejs/` package ecosystem covers most of our needs out of the box
4. Future collaborative editing support via Yjs is well-documented

## Consequences

- Team needs to learn Slate concepts (nodes, marks, normalizing)
- We'll need to maintain a markdown → Slate → markdown conversion layer
- Bundle size will be larger than Lexical alternative
- We gain a highly customizable editor that can grow with our needs

## References

- [Plate.js Documentation](https://platejs.org/)
- [Slate.js Documentation](https://docs.slatejs.org/)
- [Editor Comparison Spreadsheet](https://docs.google.com/spreadsheets/d/example)
