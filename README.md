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

### Linux

```bash
make run
```

Or:

```bash
./scripts/run_linux.sh
```

### Windows

```bat
scripts\run_windows.bat
```

Both launchers create `.venv`, install `requirements.txt`, and start `main.py`.

## Build Executables

PyInstaller builds must be created on the target OS. Build the Windows executable on Windows and the Linux binary on Linux.

### Linux

```bash
make build
```

Or:

```bash
./scripts/build_linux.sh
```

Output:

```text
dist/BeatRooter/
```

### Windows

```bat
scripts\build_windows.bat
```

Output:

```text
dist\BeatRooter\
```

## Manual Development Setup

Use this only if you want to manage the environment yourself.

### Linux/macOS Shell

```bash
python3 -m venv .venv
source .venv/bin/activate
python -m pip install --upgrade pip
python -m pip install -r requirements.txt
python main.py
```

### Windows PowerShell

```powershell
py -3 -m venv .venv
.\.venv\Scripts\Activate.ps1
python -m pip install --upgrade pip
python -m pip install -r requirements.txt
python main.py
```

## Make Targets

```text
make run    create/update .venv and start the app
make build  create/update .venv and build a local executable
make clean  remove build outputs
make help   show available commands
```

## Project Structure

```text
BeatRooter_Demo/
  main.py                         # PyQt6 entry point
  Makefile                        # Linux developer/build shortcuts
  BeatRooter.spec                 # PyInstaller build spec
  requirements.txt                # runtime dependencies
  requirements-build.txt          # build dependencies
  RUNNING.md                      # short run/build notes
  scripts/
    run_linux.sh
    build_linux.sh
    run_windows.bat
    build_windows.bat
  assets/                         # logos, icons, fonts and UI media
  features/
    app_shell/                    # welcome windows, quick menu and app shell helpers
    beatroot_canvas/              # main canvas, graph, nodes, panels and project IO
    beatnote/                     # operational notes
    cvss/                         # CVSS v4 calculator
    gnarl/                        # assistant UI and sprite handling
    language/                     # English/Portuguese catalogs
    onboarding/                   # first-run and first-investigation flows
    optimization/                 # startup/runtime optimizations
    project_backup/               # auto-backup and recovery
    shared_ui/                    # shared theme helpers
    tools/                        # tool catalog, installers, contexts and parsers
    wordlists/                    # wordlist support
  integrations/                   # optional local integration helpers
  ui/                             # compatibility import wrappers
  utils/                          # paths, images, version and platform helpers
```

## Main Dependencies

- Python 3.10+
- PyQt6
- PyQt6-WebEngine
- Pillow
- reportlab
- selenium
- webdriver-manager
- requests
- beautifulsoup4
- docker
- python-dateutil
- certifi

Build dependency:

- pyinstaller

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

## Troubleshooting

If PyQt6-WebEngine fails to start on Linux, make sure the system has the usual Qt/WebEngine runtime libraries installed.

If a build misses icons or media, rebuild with:

```bash
make clean
make build
```

If package installation fails, update pip inside the environment:

```bash
.venv/bin/python -m pip install --upgrade pip
```

On Windows:

```bat
.venv\Scripts\python -m pip install --upgrade pip
```

## License

PolyForm Shield 1.0.0

---

<div align="center">

**Map the chaos. Drive the operation. Own the evidence.**

Made by Reinvicta.

</div>
