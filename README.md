# Accessibility and Plain Language Prompt Toolkit

A toolkit for producing accessible content by translating complex text into two clear formats: Plain Language and Easy Read. Designed to help writers, editors, and AI systems produce materials that are easier to understand on the first read.

Status: Draft (private repository). See the "Publishing" section below for steps to publish this project publicly or as a website.

## Overview

Accessibility in writing is a civil right. This toolkit defines standards and a reusable system prompt that converts dense or technical text into accessible, reader-centered content.

Two levels of output are supported:

1. Plain Language (Primary): Clear, direct communication for a general audience (approx. 6th–8th grade reading level). Suitable for general documentation, product copy, and user instructions.
2. Easy Read (Alternative): Highly structured communication for people with intellectual and developmental disabilities (IDD). Focuses on literal meaning, short sentences, visual anchors, and a "Words to Know" glossary (approx. 3rd–5th grade reading level).

This prompt is compatible with plain-markdown workflows and was prepared with principles from ASAN and the google/design.md guidance in mind.

## What's in this repository

- a11y-plain-language-v1.txt — The system prompt file (copy this into the "System Instructions" or your LLM's custom instruction area).
- README.md — This file (completed and expanded).
- (Optionally) examples/ — Example inputs and outputs (add examples here to demonstrate the prompt).

If you don't see some of these files yet, you can add them to the repository to make adoption easier.

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

Add example-based tests or human-review checklists in `examples/` to ensure the prompt produces the desired outputs.

## Publishing

Below are common options for "publishing" this project. Tell me which you'd like me to do and I can perform the action for you (I can modify repo settings, enable Pages, create a release, or add common repository files). I will ask for explicit confirmation before changing repository visibility.

Option A — Make the repository public
- Go to: Settings → General → Change repository visibility → Make public.
- After making it public, others can discover and fork the project.

Option B — Publish a documentation site with GitHub Pages
- Create a `docs/` folder or use the repository root. Add an index.md (or use README as the site home).
- In the repo settings -> Pages: choose branch `main` and folder `/ (root)` or `/docs` and save.
- GitHub will build a site at `https://<your-username>.github.io/<repo-name>/` after a few minutes.

Option C — Create a Release and tag
- In the GitHub UI: Releases → Draft a new release. Choose a tag (v1.0.0) and add release notes describing the prompt and usage.
- Or use the GitHub CLI: `gh release create v1.0.0 --title "v1.0.0" --notes "Initial public release: Plain Language + Easy Read prompt"`

Option D — Add a license and contributing guidelines (recommended)
- Add LICENSE (e.g., CC-BY-4.0 for content or MIT for code). Example: `npx license mit "Your Name"` or add a LICENSE file manually.
- Add CONTRIBUTING.md with review guidance and a CODE_OF_CONDUCT.md to set community expectations.

If you want, I can:
- Make the repo public (I will ask for confirmation first).
- Enable GitHub Pages and create a basic index page for the docs site.
- Draft a release (tag + release notes).
- Add a LICENSE and CONTRIBUTING.md with recommended contents.

Which of the publishing options above would you like me to do now? If you want me to proceed with one of them, confirm which option and whether I should:
- Make the repo public (yes/no)
- Which license to add (suggestions: CC-BY-4.0 for content, MIT for code)

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

## License

No license file is included in this repository yet. Add a license to make reuse permissions explicit. If you'd like, I can add a recommended license for you.

---

If you'd like me to proceed with publishing actions (make public, enable Pages, create release, add license), tell me which options to perform and confirm whether I should change repository visibility to public. If you're unsure, tell me what outcome you want ("make a website", "share this with colleagues", "release v1") and I will recommend the exact steps and can perform them on your confirmation.
