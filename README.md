# Accessibility and Plain Language Prompt Toolkit

This repository contains a specialized system prompt designed to transform complex information into accessible content. It follows the standards established by the **Autistic Self Advocacy Network [...]

## Overview

Accessibility in writing is a civil right. This toolkit provides instructions for generating two distinct levels of accessible content:
1. **Plain Language (Primary):** Clear, direct communication for a general audience (6th–8th grade reading level).
2. **Easy Read (Alternative):** Highly structured communication for people with intellectual and developmental disabilities (IDD), focusing on literal meaning and visual anchors (3rd–5th grade re[...]

## Prompt Features

### 1. Plain Language Standards
* **Active Voice:** Clearly defines who is performing an action.
* **Direct Address:** Uses "you" and "we" to engage the reader.
* **Simplicity:** Eliminates jargon and unnecessary modifiers.
* **Organization:** Prioritizes the most important information first.

### 2. Easy Read Standards
* **One Idea Per Line:** Restricts each sentence to a single concept to reduce cognitive load.
* **Concrete Examples:** Uses third-person scenarios (e.g., "Jim does X") to make abstract concepts tangible.
* **Visual Anchors:** Includes instructions for literal icons to support visual learners.
* **Definition of Terms:** Boldens new words and requires a "Words to Know" glossary.

### 3. Design and Formatting
The prompt includes strict layout rules to prevent "walls of text":
* **Typography:** Sans-serif fonts (Open Sans) with specific leading (line spacing) requirements.
* **White Space:** Limits on paragraphs per page (maximum of 5 for Easy Read).
* **Alignment:** Strict left-alignment to prevent "rivers" of white space caused by justification.

## How to Use

1. **For AI Systems:** Copy the content of `a11y-plain-language-v1.txt` and paste it into the "System Instructions" or "Custom Instructions" field of your Large Language Model (LLM).
2. **For Manual Writing:** Use the rules in the prompt as a checklist when drafting or editing documents.
3. **Translation:** Use the prompt to "translate" existing technical or legal documents into more equitable versions.

## Validation

The provided prompt is optimized for compatibility with `@google/design.md`. To ensure your generated content or the prompt itself remains consistent with these standards, use the following lintin[...]

```bash
# Install and run the linter on your markdown files
npx @google/design.md lint YOUR_FILE.md
```

## Credits

This project was developed using guidance from the following resources and contributors:

- Autistic Self Advocacy Network (ASAN) — "One Idea Per Line: A Guide to Making Easy Read Resources" (principles adapted to inform the Easy Read standards used here).
- google/design.md — the Google Design Markdown style guides for clear, high-clarity technical writing and formatting.

Contributors:
- jscott5811 (repository owner and primary author)

If you adapted or reused material from other sources, please add them here with proper attribution and links. If you would like me to add exact links and license attributions for ASAN or google/design.md, tell me which URLs or licenses you'd prefer and I will add them.
