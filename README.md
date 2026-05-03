# Accessibility and Plain Language Prompt Toolkit

A toolkit for producing accessible content by translating complex text into two clear formats: Plain Language and Easy Read. Designed to help writers, editors, and AI systems produce materials that are easier to understand on the first read.

## Overview

Accessibility in writing is a civil right. This toolkit defines standards and a reusable system prompt that converts dense or technical text into accessible, reader-centered content.

Two levels of output are supported:

1. Plain Language (Primary): Clear, direct communication for a general audience (approx. 6th–8th grade reading level). Suitable for general documentation, product copy, and user instructions.
2. Easy Read (Alternative): Highly structured communication for people with intellectual and developmental disabilities (IDD). Focuses on literal meaning, short sentences, visual anchors, and a "Words to Know" glossary (approx. 3rd–5th grade reading level).

This prompt is compatible with plain-markdown workflows and was prepared with principles from ASAN and the google/design.md guidance in mind.

## What's in this repository

- a11y-plain-language-v1.txt — The system prompt file (copy this into the "System Instructions" or your LLM's custom instruction area).
- README.md — This file 
- examples/ — Example inputs and outputs

## How to use

1. For AI systems
   - Open `a11y-plain-language-v1.txt` and copy its content into your model's system instructions or custom instructions field.
   - Provide the model with the source text and specify which output you want: "Plain Language" or "Easy Read". Example instruction to the model: "Translate the following into Plain Language" or "Rewrite this in Easy Read format."

2. For manual writing
   - Use the prompt rules as a checklist while drafting. Key rules: use active voice, keep sentences short, put the main point first, avoid jargon, and include a "Words to Know" section for new terms.

3. For translating existing documents
   - Run your source text through the prompt to produce a first draft. Then have a human reviewer — preferably someone with accessibility expertise or lived experience — review for accuracy, tone, and cultural appropriateness.

### Example

Input (short):
"The deadline to submit your application has been moved to Friday, June 25. Late submissions will not be considered."

Plain Language output (example):
"The new deadline to send your application is Friday, June 25. We will not accept any applications sent after that date."

Easy Read output (example):
- The deadline to send your application is Friday, June 25.
- We will not accept applications after that date.

## Prompt features and standards

Plain Language standards
- Active voice (who does what).
- Direct address when appropriate ("you", "we").
- Short paragraphs and sentences; aim for 12–18 words per sentence.
- Avoid jargon and explain necessary technical terms.

Easy Read standards
- One idea per line.
- Short sentences (1 idea = 1 sentence where possible).
- Use concrete examples in the third person (e.g., "Sam clicks the button").
- Include visual anchors / icon suggestions when helpful.
- Bold new or important words; provide a "Words to Know" glossary.

Design and formatting
- Use clear headings and bulleted lists.
- Use sans-serif fonts in final formatted outputs (Open Sans recommended).
- Avoid walls of text: in Easy Read, limit to 5 short paragraphs per page where possible.

## Validation and tooling

This README recommends validating markdown using google/design.md lint rules where appropriate.

```bash
# Install and run the linter on your markdown files
npx @google/design.md lint YOUR_FILE.md
```
## About & Credits

This project adapted principles from:
- Autistic Self Advocacy Network (ASAN) — guidance on Easy Read and one-idea-per-line principles.
- google/design.md — style and markdown linting guidance for high-clarity documentation.

Contributors
- jscott5811 — repository owner and primary author

## Contributing

Contributions are welcome. Suggested first steps:
- Open an issue describing the change.
- Add examples (in `examples/`) showing before/after inputs and outputs.
- If you add files, include tests or a short review checklist.
---
