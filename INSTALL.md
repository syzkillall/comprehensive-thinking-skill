# Installation

This repository is a Codex skill. Install it by placing the repository folder under your Codex skills directory.

## Quick Install

```bash
git clone https://github.com/syzkillall/comprehensive-thinking-skill.git ~/.codex/skills/comprehensive-thinking
```

Then restart Codex so the new skill can be loaded.

## Verify Installation

Check that the skill file exists:

```bash
ls ~/.codex/skills/comprehensive-thinking/SKILL.md
```

After restarting Codex, try a prompt such as:

```text
请用全面思考帮我判断：这个复杂问题应该怎么理解？
```

If the skill is available, Codex should recognize `全面思考` / `comprehensive-thinking` as a skill trigger.

## Update

If you installed with `git clone`, update with:

```bash
cd ~/.codex/skills/comprehensive-thinking
git pull
```

Restart Codex after updating.

## Uninstall

Remove the installed skill directory:

```bash
rm -rf ~/.codex/skills/comprehensive-thinking
```

Then restart Codex.

## Custom Codex Home

If your Codex home is not `~/.codex`, install into:

```bash
$CODEX_HOME/skills/comprehensive-thinking
```

For example:

```bash
git clone https://github.com/syzkillall/comprehensive-thinking-skill.git "$CODEX_HOME/skills/comprehensive-thinking"
```

## Files Installed

The installed skill contains:

```text
SKILL.md
agents/openai.yaml
references/master-theory-research.md
examples/prompts.md
evals/quality-checklist.md
```

`SKILL.md` is the required runtime file. The other files provide UI metadata, reference material, examples, and quality checks.
