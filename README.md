# Accessibility and Plain Language Prompt Toolkit

A toolkit for producing accessible content by translating complex text into two clear formats: Plain Language and Easy Read. Designed to help writers, editors, and AI systems produce materials that are easier to understand on the first read.

## Overview

Accessibility in writing is a civil right. This toolkit defines standards and a reusable system prompt that converts dense or technical text into accessible, reader-centered content.

Two levels of output are supported:

1. Plain Language (Primary): Clear, direct communication for a general audience (approx. 6th–8th grade reading level). Suitable for general documentation, product copy, and user instructions.
2. Easy Read (Alternative): Highly structured communication for people with intellectual and developmental disabilities (IDD). Focuses on literal meaning, short sentences, visual anchors, and a "Words to Know" glossary (approx. 3rd–5th grade reading level).

This prompt is compatible with plain-markdown workflows and was prepared with principles from ASAN and the google/design.md guidance in mind.

## What's in this repository

- [a11y-plain-language-v1.txt](https://github.com/jscott5811/Accessibility-Plain-Language-Prompt-/blob/7b7596f22c8dce22a69bfc71b7caa772664ff021/a11y-plain-language-v1.txt) — The system prompt file (copy this into the "System Instructions" or your LLM's custom instruction area).
- README.md — This file 
- examples/ — Example inputs and outputs
---
name: Accessibility & Plain Language Prompt Toolkit

## Typography

The toolkit prescribes clean sans-serif fonts (like Open Sans) for all outputs to ensure maximum legibility.

- **body-md (Plain Language):** Optimized for 14pt/23pt leading equivalent.
- **body-lg (Easy Read):** Optimized for 18pt/28pt leading equivalent.

## Layout & Spacing

To prevent visual fatigue and support reading flow:
- **Alignment:** Always **left-align** text. Never justify text.
- **Spacing:** Maintain a consistent `{spacing.paragraph-gap}` between content blocks.
- **Page Limits (Easy Read):** Limit to a maximum of `{spacing.easy-read-max-paragraphs}` paragraphs per page to maintain focus.
- **Visual Anchors:** In Easy Read, every sentence or paragraph should have a literal visual anchor/icon.

## Do's and Don'ts

### Writing Style (General)
- **Do** use the active voice (who does what).
- **Do** use direct address ("you", "we") where appropriate.
- **Do** put the most important information first.
- **Don't** use jargon, acronyms, or technical terms without a "Words to Know" definition.
- **Don't** use metaphors, idioms, or abstract sarcasm.

### Formatting (Easy Read)
- **Do** limit each line to one idea.
- **Do** use concrete examples in the third person (e.g., "Sam clicks the button").
- **Do** bold important terms the first time they appear.
- **Don't** exceed 15 words per sentence for high-accessibility contexts.

## How to Use

### 1. For AI Systems
Copy the content of `a11y-plain-language-v1.txt` into your model's system instructions. 
Specify the desired output format in your prompt: *"Rewrite the following in Plain Language"* or *"Translate this to Easy Read."*

### 2. For Manual Writing
Use the rules in this document as a checklist. Focus on the active voice and the "Words to Know" glossary for any technical concepts.

### 3. Validation
Validate your documentation for style and consistency using the following command:

```bash
npx @google/design.md lint DESIGN.md
```

## Contributing

Contributions are welcome. Please open an issue describing your proposed changes and include examples in the `examples/` directory showing before/after results.

## About & Credits

This project adapted principles from:
- [Autistic Self Advocacy Network (ASAN)](https://autisticadvocacy.org/resources/accessibility/easyread/) — guidance on Easy Read and one-idea-per-line principles.
- [google/design.md](https://github.com/google-labs-code/design.md.git) — style and markdown linting guidance for high-clarity documentation.

Contributors
- jscott5811 — repository owner and primary author

## Contributing

Contributions are welcome. Suggested first steps:
- Open an issue describing the change.
- Add examples (in `examples/`) showing before/after inputs and outputs.
- If you add files, include tests or a short review checklist.
---
