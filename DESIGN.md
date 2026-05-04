---
version: alpha
name: Accessibility & Plain Language
colors:
  primary: "#1A1A1A"
  secondary: "#005A9C"
  neutral: "#FFFFFF"
  surface: "#F5F5F5"
typography:
  body-md:
    fontFamily: Open Sans
    fontSize: 18.67px
    fontWeight: 400
    lineHeight: 1.6
    letterSpacing: 0.01em
  body-lg:
    fontFamily: Open Sans
    fontSize: 24px
    fontWeight: 400
    lineHeight: 1.5
    letterSpacing: 0.01em
spacing:
  xs: 4px
  md: 16px
  paragraph-gap: 24px
  easy-read-limit: 5
rounded:
  sm: 4px
---

# Accessibility & Plain Language Design System

## Overview

This system defines standards for **Plain Language** and **Easy Read** formats. The primary goal is to eliminate cognitive barriers, making information clear and direct for the widest possible audience, including users with cognitive disabilities or low literacy levels.

## Colors

The palette prioritizes high contrast to ensure WCAG AAA compliance and reduce eye strain.

- **Primary ({colors.primary}):** A near-black ink used for all body text to ensure maximum contrast against light backgrounds.
- **Secondary ({colors.secondary}):** A deep accessible blue used for links and primary interactive indicators.
- **Neutral ({colors.neutral}):** Pure white is the standard background to maintain clarity, though soft surfaces may be used for grouping.

## Typography

Readability is driven by clean sans-serif typefaces and generous line heights.

- **Plain Language (body-md):** Designed for a 6th–8th grade reading level. Uses `{typography.body-md.fontSize}` for standard clear communication.
- **Easy Read (body-lg):** Designed for a 3rd–5th grade reading level. Uses `{typography.body-lg.fontSize}` to support users with significant cognitive or visual processing needs.

## Layout

Layouts are strictly structured to prevent visual fatigue and support a linear reading flow.

- **Alignment:** All text blocks must be **left-aligned**. Justified text is prohibited as it creates "rivers of white" that disrupt reading.
- **Spacing:** A standard gap of `{spacing.paragraph-gap}` is maintained between blocks to provide visual breathing room.
- **Constraints:** Easy Read pages are limited to a maximum of `{spacing.easy-read-limit}` paragraphs per view.

## Shapes

To maintain a professional yet approachable aesthetic, subtle rounding is used on containers.

- **Containers:** Informational cards and callouts utilize `{rounded.sm}` corner radius to soften the interface without losing structural clarity.

## Do's and Don'ts

### Writing Style
- **Do** use the active voice and direct address ("you").
- **Do** keep sentences between 10 and 15 words.
- **Don't** use jargon, metaphors, or idioms.
- **Don't** use "click here" — use descriptive action labels.

### Formatting & Icons
- **Do** provide one clear, literal icon per sentence in Easy Read formats.
- **Do** bold important terms the first time they appear.
- **Don't** use abstract or metaphorical icons.
- **Don't** use all-caps for long strings of text; it reduces word-shape recognition.
