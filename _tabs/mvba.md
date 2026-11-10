---
title: MVBA
icon: fas fa-diagram-project
order: 3
---

**MultiValue Basic Analyser (MVBA)** is a Visual Studio Code extension that generates documentation reports for Rocket **UniVerse** BASIC programs, including the internal call tree with Mermaid or Markmap diagrams, file usage, metrics and warnings.

It is free.

[Get it from the VS Code Marketplace](https://marketplace.visualstudio.com/items?itemName=LXie.multivalue-basic-analyser){: .btn .btn-primary }

## What the report contains

| Section | What it shows |
|---|---|
| **Call tree** | The program's internal call structure, drawn as a Mermaid or Markmap diagram |
| **File usage** | The files the program uses |
| **Metrics** | Measurements of the program |
| **Warnings** | Points in the code that deserve a second look |

## Usage

1. Open a UniVerse BASIC program in VS Code.
2. Open the Command Palette (Ctrl+Shift+P, or Cmd+Shift+P on macOS).
3. Run **MultiValue Basic Analyser: Analyse Program**.

## Settings

Open **Settings** and search for "MultiValue Basic Analyser".

## Installation

- **From the Marketplace**: in VS Code, open **Extensions**, search for *MultiValue Basic Analyser* and click **Install**.
- **From a VSIX file**: in the Extensions view, select the **…** menu, choose **Install from VSIX…** and select the file. Or run:

  ```sh
  code --install-extension multivalue-basic-analyser-1.0.0.vsix
  ```

## Supported dialects

MVBA is designed for Rocket UniVerse BASIC. Other MultiValue dialects, including UniData BASIC, have not been tested.

## Why it helps modernization

Before changing a program that has run for decades, a team needs to know what it calls and which files it touches. An MVBA report gives that map, in a form that can be reviewed and kept with the code.

See also [MVBU]({{ '/mvbu/' | relative_url }}), for looking at the data those programs work on.

UniVerse is a product of Rocket Software.
