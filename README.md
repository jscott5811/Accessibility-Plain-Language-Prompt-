# Accessibility and Plain Language Prompt Toolkit

A toolkit for producing accessible content by translating complex or technical text into two clear formats: Plain Language and Easy Read. This project provides a system prompt, design guidance, and examples to help writers and AI systems produce accessible, reader-centered content.

## Overview

Accessibility in writing is a civil right. This toolkit defines standards and a reusable system prompt that converts dense or technical text into accessible, reader-centered content.

Two levels of output are supported:

1. Plain Language (Primary): Clear, direct communication for a general audience (approximately 6th–8th grade reading level). This format is suitable for general documentation, product copy, and instructional content.
2. Easy Read (Alternative): Highly structured communication intended for people with intellectual and developmental disabilities (IDD) and other readers who benefit from literal wording, short sentences, and visual anchors.

This prompt and guidance are compatible with plain-markdown workflows and were prepared using best-practice principles from disability advocacy groups and established design guidance.

## What's in this repository

- [a11y-plain-language-v1.md](https://github.com/jscott5811/Accessibility-Plain-Language-Prompt-/blob/main/a11y-plain-language-v1.md) — The system prompt file used by AI and human workflows.
- [docs/a11y-plain-language-v1.md](https://github.com/jscott5811/Accessibility-Plain-Language-Prompt-/blob/main/docs/a11y-plain-language-v1.md) — Rendered copy of the system prompt for GitHub Pages.
- README.md — This file (documentation and usage guidance).
- DESIGN.md — Design system specifying colors, typography, spacing, layout rules, and guidelines for Plain Language and Easy Read formats. See [DESIGN.md](https://github.com/jscott5811/Accessibility-Plain-Language-Prompt-/blob/main/DESIGN.md).
- examples/ — Example inputs and outputs demonstrating how to translate text into Plain Language and Easy Read formats.

---

name: Accessibility & Plain Language Prompt Toolkit

## Typography

The toolkit prescribes clean sans-serif fonts (for example, Open Sans) for all outputs to ensure maximum legibility.

- body-md (Plain Language): Optimized for text sized for general reading—roughly 14px–16px on screen with comfortable line height.
- body-lg (Easy Read): Larger text (roughly 18px–24px) with increased line height for users who need bigger type and more vertical spacing.

## Layout & Spacing

To prevent visual fatigue and support a clear reading flow:
- Alignment: Always left-align text. Never justify text because justification can create uneven word spacing that makes reading harder.
- Spacing: Maintain a consistent gap of 24px between content blocks to provide visual breathing room.
- Page limits (Easy Read): Keep Easy Read pages short—limit content to a maximum of 5 paragraphs per view to avoid overloading the reader.
- Visual anchors: In Easy Read, provide a literal visual anchor (an icon or simple image) for each sentence or paragraph to reinforce meaning and aid memory.

## Do's and Don'ts

### Writing Style (General)
- Do use the active voice (who does what).
- Do use direct address ("you", "we") where appropriate to make instructions clearer.
- Do put the most important information first (in the opening sentence or lead).
- Don't use unexplained jargon, acronyms, or technical terms—provide a short "Words to Know" definition when they are necessary.
- Don't use metaphors, idioms, or abstract sarcasm, which can be confusing for many readers.

### Formatting (Easy Read)
- Do limit each line or sentence to a single idea.
- Do use concrete examples in the third person (for example, "Sam clicks the button") to show actions clearly.
- Do bold important terms the first time they appear.
- Don't exceed 15 words per sentence in high-accessibility contexts; shorter sentences improve comprehension.
- Do include a simple image or icon beside each key sentence to provide a visual anchor.

## How to Use

### 1. For AI Systems
Copy the content of `a11y-plain-language-v1.txt` into your model's system instructions. When calling the model, specify the desired output format in your prompt:
- "Rewrite the following in Plain Language"
- "Translate this to Easy Read"

The prompt file includes rules for sentence length, voice, structure, and formatting that the model should follow when generating output.

### 2. For Manual Writing
Use the rules in this document as a checklist. Focus on the active voice, one idea per sentence for Easy Read, and a "Words to Know" glossary for any technical concepts.

### 3. Validation
Validate your documentation for style and consistency using the following command:

```bash
npx @google/design.md lint DESIGN.md
```

(That runs the google/design.md linter against DESIGN.md and flags formatting or structure issues; adjust files accordingly.)

## Contributing

Contributions are welcome. Please open an issue describing your proposed changes and include example files in the `examples/` directory showing before/after inputs and outputs.

If you propose changes to DESIGN.md, describe the accessibility reasoning for each change and include sample renderings if possible.

## About & Credits

This project adapted principles from:
- Autistic Self Advocacy Network (ASAN) — Guidance on Easy Read and one-idea-per-line principles: https://autisticadvocacy.org/resources/accessibility/easyread/
- google/design.md — Style and markdown linting guidance for high-clarity documentation: https://github.com/google-labs-code/design.md.git

Contributors:
- jscott5811 — Repository owner and primary author

---
