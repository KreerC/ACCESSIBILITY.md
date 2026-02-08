# ACCESSIBILITY.md

This repository is home to [a skill](https://agentskills.io) for your AI agents to ensure they develop accessible codebases.

It is highly recommended to **conduct periodic manual accessibility reviews**. This can include tasks like navigating the site with a screen reader (e.g., NVDA or VoiceOver) to ensure content is read in a sensible order, testing all functions with only the keyboard, and trying high-contrast or zoom settings to see if the UI remains usable. Especially in cases where AI agents are doing most of the development work, engaging an accessibility expert or beta users with disabilities to evaluate the product can provide critical feedback. Manual testing validates the real user experience and catches nuances that rules-based checkers might miss.

## Installation

### Any agent

Ask your Agent (Claude Code, Codex, Opencode, ...) to install this globally, with a link to the repository.

```txt
Install the skill from https://github.com/KreerC/ACCESSIBILITY.md globally.
```

Check your agents' documentation for specific documentation, or [read about the integration details of the official docs.](https://agentskills.io/integrate-skills)

### Codex

Run this one-liner to download the latest `main.zip` from GitHub and install the `accessibility` skill globally into `/etc/codex/skills`.

```bash
TMP_DIR="$(mktemp -d)" && curl -fsSL "https://github.com/KreerC/ACCESSIBILITY.md/archive/refs/heads/main.zip" -o "$TMP_DIR/main.zip" && unzip -q "$TMP_DIR/main.zip" -d "$TMP_DIR" && sudo mkdir -p /etc/codex/skills/accessibility && sudo cp -R "$TMP_DIR/ACCESSIBILITY.md-main/accessibility" /etc/codex/skills/accessibility && rm -rf "$TMP_DIR"
```

This will make sure the skill is available everywhere in Codex and automatically considered for all projects.
