# Gemini Write

A skill for Codex and Claude Code that uses Gemini to write, rewrite, and proofread text. It works with text files such as Markdown. It edits a copy of your draft and applies changes to the original file only after checking the results.

## Setup

### 1. Install Antigravity CLI

macOS / Linux:

```bash
curl -fsSL https://antigravity.google/cli/install.sh | bash
```

Windows (PowerShell):

```powershell
irm https://antigravity.google/cli/install.ps1 | iex
```

After installation, reopen your terminal and run:

```bash
agy
```

Follow the on-screen instructions to log in, then exit with `/exit`. Setup is complete when the following command displays the list of models:

```bash
agy models
```

For details, see the [official installation instructions](https://antigravity.google/docs/getting-started#download-and-install) and [login guide](https://antigravity.google/docs/install?tab=cli).

### 2. Install this skill

This installation command requires Node.js 22.20 or later and npm.

```bash
npx skills add laiso/gemini-write --skill gemini-write -g
```

Follow the displayed prompts to select the agent you want to use.

## Usage

Codex:

```text
$gemini-write make draft.md more readable while preserving its content and tone
```

Claude Code:

```text
/gemini-write fix only typos and grammar in draft.md
```

If no model is specified, it selects the latest available Gemini Flash (Medium). If processing fails, changes are not applied and the reason is reported.

This document was created with Gemini Write.
