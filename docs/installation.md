# Installation and first use

[العربية](installation.ar.md) · [Home](../README.md)

Copy **`skills/work-to-video-script/` with all its contents**, not only `SKILL.md`. The instructions use two sibling reference files. You need an agent/model, access to the relevant completed work, and a permitted private output location. Genuine new screenshots also require a browser/app capture tool; without one, the pack reports the missing captures.

## Route 1 — ask an agent with file-install capability

```text
Install work-to-video-script from
https://github.com/eyoussef-builds/work-to-video-script/tree/main/skills/work-to-video-script
in your documented personal skills location. Keep the references and agents folder.
If that name already exists, inspect it and preserve local changes before updating.
Then read SKILL.md and confirm that its two references are available.
```

An agent unable to download files needs the manual route. Installing a skill does not authorize access to private accounts or unrelated data.

## Route 2 — manual download/copy

Download [the source ZIP](https://github.com/eyoussef-builds/work-to-video-script/archive/refs/heads/main.zip). On macOS, double-click it; on Windows, right-click → Extract All. Open the extracted folder and copy `skills/work-to-video-script` to the appropriate root below. Hidden folders may need to be created.

### macOS/Linux — Codex example

From a folder where you want the source checkout:

```sh
git clone https://github.com/eyoussef-builds/work-to-video-script.git
skill_destination="$HOME/.agents/skills/work-to-video-script"
if [ -e "$skill_destination" ]; then
  printf '%s\n' 'Already installed; review local changes before updating.'
  exit 1
fi
mkdir -p "$HOME/.agents/skills"
cp -R work-to-video-script/skills/work-to-video-script "$skill_destination"
```

### Windows PowerShell — Codex example

After extracting the ZIP, open PowerShell in the extracted repository:

```powershell
$skillDestination = Join-Path $HOME '.agents/skills/work-to-video-script'
if (Test-Path $skillDestination) { throw 'Already installed; review local changes before updating.' }
New-Item -ItemType Directory -Force (Split-Path $skillDestination) | Out-Null
Copy-Item -Recurse './skills/work-to-video-script' $skillDestination
```

Use the same copy operation with another agent's documented destination. `~` means your home directory; use `$HOME` or the folder browser on Windows. Do not run POSIX shell commands in PowerShell unchanged.

## Agent routes

Official documentation was checked on **2026-10-25**. “Native” below describes documented skill discovery, not a completed end-to-end test of this skill in that product. Screenshot/history access still depends on host tools. Paths name the **root**; put `work-to-video-script/` beneath it.

| Agent | Personal root | Project root / alternative | Invoke and check | Official source |
| --- | --- | --- | --- | --- |
| Codex | `~/.agents/skills/` | `.agents/skills/` | Ask for `$work-to-video-script`; inspect skills selector or ask for its loaded file | [Skills](https://learn.chatgpt.com/docs/build-skills) |
| Claude Code | `~/.claude/skills/` | `.claude/skills/` | `/work-to-video-script`; inspect slash menu | [Skills](https://code.claude.com/docs/en/skills) |
| OpenClaw | `~/.openclaw/skills/` | Workspace `skills/` | Ask to use the skill; inspect `openclaw skills list` | [Skills](https://docs.openclaw.ai/tools/skills) |
| Hermes Agent | `~/.hermes/skills/` | Configure an external skill directory when project scope is needed | Ask to load the skill and show its source | [Skills](https://hermes-agent.nousresearch.com/docs/user-guide/features/skills) |
| Cursor | `~/.cursor/skills/` or `~/.agents/skills/` | `.cursor/skills/` or `.agents/skills/` | Ask Agent to use the named skill and identify its source | [Skills](https://cursor.com/docs/skills) |
| Grok Bot | Explicit instruction import in this guide | Supply the skill and both references to the Bot's accessible workspace | Ask it to read all three files for this task; no native install/phrase-listener claim | [Bot context](https://cursor.com/docs/grok-bot) |
| OpenCode | `~/.config/opencode/skills/` | `.opencode/skills/` or `.agents/skills/` | Ask to load with the native skill tool and identify its source | [Skills](https://opencode.ai/docs/skills/) |
| GitHub Copilot | `~/.copilot/skills/` or `~/.agents/skills/` | `.github/skills/` or `.agents/skills/` | Ask agent mode to load the skill; availability varies by client/version | [Skills](https://docs.github.com/en/copilot/concepts/customizations/agent-skills) |
| Gemini CLI | `~/.gemini/skills/` or `~/.agents/skills/` | `.gemini/skills/` or `.agents/skills/` | `gemini skills list --all`; ask to use the named skill | [Skills](https://geminicli.com/docs/cli/skills/) |
| Windsurf / Cascade / Devin Desktop | `~/.codeium/windsurf/skills/` or `~/.config/devin/skills/` | `.devin/skills/`; legacy `.windsurf/skills/` | Select it through Cascade Skills / @mention; confirm its loaded source | [Cascade skills](https://docs.devin.ai/desktop/cascade/skills) |
| Cline | `~/.cline/skills/` | `.cline/skills/` | Find it in Skills; select `/work-to-video-script` | [Skills](https://docs.cline.bot/customization/skills) |
| Roo Code | `~/.roo/skills/` | `.roo/skills/` | Ask Roo to load the named skill and show its source | [Skills](https://roocodeinc.github.io/Roo-Code/features/skills/) |
| Aider | Explicit read-only instruction import | Add `SKILL.md` and both references as read-only context for this task | Request the workflow explicitly; arrange screenshot capture outside Aider if needed | [Read-only conventions](https://aider.chat/docs/usage/conventions.html) |
| Amp | `~/.config/agents/skills/` or `~/.agents/skills/` | `.agents/skills/` | `amp skills list`; ask to reload skills in the active thread | [Skills](https://ampcode.com/docs/customize/skills) |
| Goose | `~/.agents/skills/` | `.agents/skills/` | `goose skills list` or `/skills work-to-video-script` | [Maintained skill guide](https://github.com/aaif-goose/goose/blob/main/documentation/docs/guides/context-engineering/using-skills.md) |

For the two instruction-import routes, say:

```text
Read SKILL.md, references/evidence-guide.md and references/deliverable-template.md
from the supplied work-to-video-script folder as instructions for this task.
The completed work is approved. Draft its story, real screenshot pack and demo plan.
State capture/history limits and stop before producing the video.
```

Do not append this workflow to global rules merely to emulate automatic selection. A host may support other native routes; this guide does not assert their absence.

## First use and discovery

Ask the agent to locate the skill, read it and name its two references. If it is absent, check the folder nesting, enabled skills and the selected workspace/session. Refresh/restart discovery according to the host. Remote/cloud environments need the package and project evidence in their own accessible filesystem; local personal skills are not automatically synced.

```text
All good. Use work-to-video-script for the completed project in this task.
Narrate in my preferred language with my approved avatar.
Use real screenshots, mark missing footage and include a concrete demo plan.
Do not generate voice or video and do not execute the live demo.
```

Set optional narrator/language/brand preferences in a local `references/local-profile.md`. Keep it private and outside the public package. A task-specific language choice overrides the profile. Do not include keys, accounts or customer information there.

## Updating and uninstalling

Download changes into a separate folder, compare the skill and references, back up and preserve your local profile/customizations, then replace only the intended installed files. Do not merge arbitrary upstream instructions without review. Remove only the installed `work-to-video-script` folder to uninstall and refresh the host's discovery. Private evidence/output files are separate; delete them deliberately under your retention policy.

## Verification scope

This release checks skill metadata, reference integrity, public-package contents, documentation links and reviewer scenarios. The instructions were authored in Codex; this is not a 15-agent execution certification or a guarantee that “all good” always auto-selects it. There is no bundled installer, collector, background service or new account connection.
