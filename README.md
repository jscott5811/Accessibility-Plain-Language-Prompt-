# Accessibility and Plain Language Prompt Toolkit

This repository contains a specialized system prompt designed to transform complex information into accessible content. It follows the standards established by the **Autistic Self Advocacy Network (ASAN)** in their guide, *One Idea Per Line: A Guide to Making Easy Read Resources*.

## Overview

Accessibility in writing is a civil right. This toolkit provides instructions for generating two distinct levels of accessible content:
1. **Plain Language (Primary):** Clear, direct communication for a general audience (6th–8th grade reading level).
2. **Easy Read (Alternative):** Highly structured communication for people with intellectual and developmental disabilities (IDD), focusing on literal meaning and visual anchors (3rd–5th grade reading level).

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

The provided prompt is optimized for compatibility with `@google/design.md`. To ensure your generated content or the prompt itself remains consistent with these standards, use the following linting tool:

```bash
# Install and run the linter on your markdown files
npx @google/design.md lint YOUR_FILE.md

## Credits

This prompt was developed based on the accessibility research and standards provided by the Autistic Self Advocacy Network (ASAN) One Idea Per Line: A Guide to Making Easy Read Resources
and the @google/design.md documentation style guides used for high-clarity technical design.
