---
layout: default
title: "Accessibility Statement"
permalink: /accessibility-statement/
description: "We're committed to great accessibility on the Blind Arduino site."
---

## Our Commitment

This site is built and maintained by and for blind and low-vision makers.

We try to conform to the [Web Content Accessibility Guidelines (WCAG) 2.1](https://www.w3.org/TR/WCAG21/) at Level AA.

## What We Do

- Provide a skip link so keyboard and screen reader users can jump past navigation directly to the main content
- Use proper HTML landmark elements (`<header>`, `<nav>`, `<main>`, `<footer>`) for easy navigation
- Maintain a strict heading hierarchy with one `<h1>` per page
- Mark the current page in navigation with `aria-current="page"`
- Move focus to the first content heading on page load
- Ensure all images have descriptive `alt` text
- Open external links in a new tab with an audible notice ("opens in new tab")
- Support system light/dark mode preference
- Use a minimum body font size of 16px and a content width of no more than ~72 characters
- Test with NVDA and Chrome

## Known Issues

None currently known. If you find a barrier, please let us know using the contact information below.

## Feedback

If you encounter any accessibility issues on this site, please [contact us]({{ "/contact/" | relative_url }}). We take all reports seriously and aim to respond within five business days.

## Review Date

This statement was last reviewed {{ site.time | date: "%B %Y" }}.
