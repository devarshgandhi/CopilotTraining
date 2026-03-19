---
applyTo: "slides/**/*.md"
description: "Use when editing Slidev deck markdown files, section opener slides, or raw HTML in slides. Covers balanced HTML, wrapper structure, and required deck build validation."
---

# Slidev Deck Editing

- Treat Slidev markdown as Vue template code whenever a slide includes raw HTML. Every opened tag must have a matching closing tag before the next `---` slide separator.
- Prefer one obvious outer wrapper for custom section-opener slides. Avoid deeply nested wrapper stacks unless they are necessary for layout.
- When inserting or rearranging blocks, account for wrapper balance explicitly instead of relying on visual scanning.
- After every edit to a Slidev deck, run the build for that specific deck before concluding the task. Editor diagnostics are not sufficient to catch all Vue or Slidev parse errors.
- If a build fails with `Element is missing end tag` or `Invalid end tag`, inspect the most recently edited slide first and verify wrapper balance from outermost container to innermost content.
