<p align="center"><img src="docs/images/hero.svg" alt="Work to Video Script: completed work, real evidence, a narrated script and demo plan" width="100%"></p>

# Work to Video Script

**You finished the project. Now tell the story—with proof.**

[العربية](README.ar.md) · [Install](docs/installation.md) · [Privacy](docs/privacy.md) · [Example](docs/example.md) · [Share pack](docs/sharing.md)

You built something with an AI assistant. The useful story is scattered across decisions, commits, test results and screenshots. This skill brings those pieces together into a narrated video script, a real screenshot pack and a practical demo recording plan.

Say **“All good—write the story.”** after approving the completed work. Review the script before choosing whether to make a video.

## From finished work to a reviewable story

1. **Review the work.** The agent checks the active task, requirements, relevant changes and actual verification records.
2. **Collect the evidence.** It inspects existing screenshots and can take authorized read-only captures of the actual application. Missing footage stays visibly missing.
3. **Write and plan.** It drafts the narration and scenes, links important claims to evidence, and specifies the later demo actions.
4. **You review.** Voice generation, avatar animation, video recording/rendering and publishing require a separate instruction.

![English skill explainer](docs/images/infographic-en.png)

## What you receive

| Output | Why it helps |
| --- | --- |
| Narrated script + storyboard | Exact spoken copy, approximate scene timings and on-screen actions |
| Real screenshot pack + index | Inspectable images linked to the scenes, with capture provenance |
| Private evidence ledger | A source for each important claim, including verification limits |
| Demo plan | Starting state, exact inputs, visible results, waits, side effects and cleanup |
| Capture gaps | An honest list of footage/access still needed |

Useful for builders, developers and creators explaining a completed project. An approved avatar can narrate; the skill does not include an avatar model or voice.

## Install and try it

### Ask your agent

```text
Install the work-to-video-script skill from
https://github.com/eyoussef-builds/work-to-video-script/tree/main/skills/work-to-video-script
for this agent. Preserve the supporting references and existing local customizations.
```

This route requires an agent that can download and install local files. Review any host permission request.

### Copy the folder yourself

Download the [source ZIP](https://github.com/eyoussef-builds/work-to-video-script/archive/refs/heads/main.zip), unzip it, and copy **the whole `skills/work-to-video-script` folder** into your agent's skills directory. For current Codex, the shared user location is `~/.agents/skills/`; Claude Code uses `~/.claude/skills/`. See the [15-agent installation guide](docs/installation.md) for paths, Windows steps, discovery and instruction-import alternatives.

Then try:

```text
All good. Use $work-to-video-script for the project we just completed.
Write a first-person script with real screenshots and a demo plan.
Use my approved avatar and language. Do not create the video.
```

**Discovery check:** ask the agent to locate `work-to-video-script`, read its `SKILL.md` and name its two supporting references. A file copied to your laptop does not automatically become available in a cloud agent.

## Your first story

1. Finish the underlying project and approve its result.
2. Keep the relevant workspace, conversation and existing verification records available to the agent.
3. Ask for the story. It scans the active project, rather than unrelated repos or inboxes.
4. Inspect the script and linked screenshots. Anything requiring a real message, production write or paid call remains in the later demo plan unless separately authorized.
5. Revise the script. Decide on video production separately.

The [fictional example](docs/example.md) shows how a “tests passed” claim differs from a real deployment and how a missing screenshot is reported.

## What “all good” means

The trigger is contextual: approval of completed project work. It is not a global listener, scheduled scan or screen recorder. A casual acknowledgment, an intermediate choice, or approval of the resulting script does not recursively create another story. If automatic selection is unavailable, invoke the skill explicitly.

## Privacy and access

The skill contains instructions and templates, with no bundled executable collector, account connection or required API key. Your host agent/model still processes the material you give it, and any connected capture services retain their own permissions and policies. Agent usage may cost money under your plan/provider.

Raw screenshots, source mappings and the evidence ledger stay in private project outputs. Only separately reviewed crops/redactions belong in a shareable pack. Installing the skill does not grant access to other agents' histories, your whole computer, private accounts or external recipients. [Read the privacy guide](docs/privacy.md).

<details>
<summary>Can it recreate screen recordings from before it was installed?</summary>

It can recover the story from available records and historical screenshots. It cannot invent a recording of clicks that were never captured. Current captures and later demos are labeled as such.
</details>

<details>
<summary>Does it make or publish the video?</summary>

No. It stops at the script, screenshots and demo plan. A script approval alone does not authorize voice generation, animation, recording, rendering, publishing or live demo messages.
</details>

<details>
<summary>Will it work in every agent?</summary>

The portable instructions can be loaded in skills-capable agents or supplied as explicit instructions. Actual access to task history, files, browser screenshots and private output folders depends on the host. Installation documentation is not a claim of end-to-end testing in every listed product.
</details>

<details>
<summary>Can I choose my own narrator and language?</summary>

Yes. Provide them in the request or an optional private `references/local-profile.md` inside your installed copy. Keep that profile out of public exports. The distributed skill has no personal account bindings or avatar artwork.
</details>

## Inside the package

```text
skills/work-to-video-script/
├── SKILL.md
├── agents/openai.yaml
└── references/
    ├── evidence-guide.md
    └── deliverable-template.md
```

No runtime dependency or bundled scanning script. Structural validation, source review and the documented [behavioral review cases](docs/behavioral-review.md) cover the instruction package; cross-agent execution is not claimed.

## License and sharing

[MIT](LICENSE). You can use and adapt the skill; host/service charges are separate. [English and Arabic infographics, Facebook artwork and draft announcement copy](docs/sharing.md) are included. These promotional illustrations explain the skill; they are not screenshots proving a real project outcome.

Published by [eyoussef-builds](https://github.com/eyoussef-builds).
