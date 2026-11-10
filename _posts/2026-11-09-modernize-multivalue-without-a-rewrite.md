---
title: "Modernize MultiValue without rewriting it"
date: 2026-11-09 09:00:00 +0000
categories: [MultiValue, Modernization]
tags: [universe, unidata, mvbu, mvba]
pin: true
---

UniVerse and UniData systems often run the core of a business, and they usually run it well. What ages is everything around them: 24 × 80 terminals, reports that wrap, subroutines nobody can easily test, and BASIC code that only a few people still understand.

Modernizing doesn't have to mean a rewrite. It can mean better windows onto the data and better maps of the code.

## A path in four steps

1. **See**: put data, schema and API results in front of the whole team.
2. **Understand**: map programs, calls and file usage before touching anything.
3. **Expose**: turn well-understood subroutines into documented APIs.
4. **Evolve**: refactor or replace the parts that matter, with evidence of what depends on them.

## MVBU: see the data

[MultiValue Basic Utility](https://chromewebstore.google.com/detail/heepofiejichbhogampmkghinpgjilpa) runs in Chrome, Edge and VS Code. It offers:

- a Developer console for TCL/ECL commands at `TERM 132,999`
- API calls to catalogued subroutines, with dynamic arrays broken down by field, value and sub-value
- an Analyst view in plain language: look up a record, find records, see what's in a file
- every run saved as Markdown

A small Python helper on your own computer connects through Rocket uopy (UniRPC over SSL), so nothing is installed on the database server.

```text
MVBU page (Chrome) ──native messaging──▶ MVBU helper (Python + uopy) ──UniRPC / SSL──▶ UniVerse / UniData
```

## MVBA: understand the code

[MultiValue Basic Analyser](https://marketplace.visualstudio.com/items?itemName=LXie.multivalue-basic-analyser) is a VS Code extension that generates documentation reports for Rocket UniVerse BASIC programs, including the internal call tree with Mermaid or Markmap diagrams, file usage, metrics and warnings.

Open a program in VS Code and run **MultiValue Basic Analyser: Analyse Program** from the Command Palette.

## Read more

- [Technical edition]({{ '/mv-modernization/technical/' | relative_url }}): architecture and safeguards
- [Learn MultiValue]({{ '/mv-modernization/learn/' | relative_url }}): the basics, explained simply
