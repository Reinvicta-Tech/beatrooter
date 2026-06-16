<p align="center">
  <img src="./assets/beatrooter_logo.svg" width="220" alt="BeatRooter logo">
</p>

<p align="center">
  <img src="https://img.shields.io/badge/license-Educational%20Use-blue.svg" alt="License">
  <img src="https://img.shields.io/badge/platform-Linux%20%7C%20Windows-lightgrey.svg" alt="Platform">
  <img src="https://img.shields.io/badge/python-3.10%2B-blue.svg" alt="Python">
  <img src="https://img.shields.io/badge/version-demo%200.6.0-923A5F.svg" alt="Demo version 0.6.0">
  <img src="https://img.shields.io/badge/ui-PyQt6-8b5cf6.svg" alt="PyQt6">
</p>

<p align="center">
  <strong>Beat roots. Beat them all. Be a BeatRooter.</strong>
</p>

---

# BeatRooter Demo

BeatRooter is a PyQt6 desktop demo for visually organizing cybersecurity investigations. It gives you a canvas where assets, observations, evidence, notes and tool results can be mapped as connected nodes instead of being scattered across terminals, files and screenshots.

This repository is the demo build. Experimental modules and unfinished product lines were removed from the user-facing workflow so the app stays focused on the investigation canvas.

## What Is Included

- Visual investigation canvas with draggable nodes and dynamic edges.
- Atomic node library for assets, observations, evidence, findings, actions and notes.
- Custom node templates for adapting the canvas to a specific lab or workflow.
- Stackers for grouping related canvas items.
- Detail panel for editing node data and relationships.
- BeatNote for operational notes and documentation.
- CVSS v4 calculator.
- Gnarl assistant panel and visual UI elements.
- External tool management and command-oriented tool nodes.
- English and Portuguese UI catalogs.
- Project save/open/export support for `.brt` and JSON workflows.
- Auto-backup and recovery support for active investigations.

## Quick Start

In [realeses](https://github.com/Reinvicta-Tech/beatrooter/releases) ownload the [demo.zip](https://github.com/Reinvicta-Tech/beatrooter/releases/download/v0.6/Demo.zip) file

For **Linux** and **Windows**

## Basic Workflow

1. Start a new investigation or open an existing `.brt` file.
2. Add atomic nodes for assets, observations, evidence, findings, actions or notes.
3. Connect nodes to make relationships clear.
4. Use the detail panel to enrich each node.
5. Use BeatNote for supporting notes.
6. Run tool nodes when you need external command output.
7. Save or export the project.

## Responsible Use

BeatRooter is intended for education, labs, CTFs, internal security work and explicitly authorized assessments. Some integrated tools can generate offensive traffic or handle sensitive artifacts.

Use it only in systems you own, lab environments, CTFs, wargames, or authorized audits. Do not use BeatRooter to attack, test or enumerate third-party systems without permission.

## License

PolyForm Shield 1.0.0

---

<div align="center">

**Map the chaos. Drive the operation. Own the evidence.**

Made by Reinvicta.

</div>
