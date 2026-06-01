# Installation

This repository is an Agent Skill. It can be installed in Codex and Claude because the repository root contains the required `SKILL.md` file.

## Install For Codex

Install as a personal Codex skill:

```bash
git clone https://github.com/syzkillall/comprehensive-thinking-skill.git ~/.codex/skills/comprehensive-thinking
```

Then restart Codex so the new skill can be loaded.

If your Codex home is not `~/.codex`, install into `$CODEX_HOME/skills/comprehensive-thinking`:

```bash
git clone https://github.com/syzkillall/comprehensive-thinking-skill.git "$CODEX_HOME/skills/comprehensive-thinking"
```

Verify the install:

```bash
ls ~/.codex/skills/comprehensive-thinking/SKILL.md
```

## Install For Claude Code

Install as a personal Claude Code skill:

```bash
git clone https://github.com/syzkillall/comprehensive-thinking-skill.git ~/.claude/skills/comprehensive-thinking
```

This makes the skill available across your Claude Code projects. The directory name controls the slash command, so this installs the command as:

```text
/comprehensive-thinking
```

You can also install it only for one project:

```bash
mkdir -p .claude/skills
git clone https://github.com/syzkillall/comprehensive-thinking-skill.git .claude/skills/comprehensive-thinking
```

Verify the install:

```bash
ls ~/.claude/skills/comprehensive-thinking/SKILL.md
```

If Claude Code was already running and the top-level skills directory did not exist before, restart Claude Code. Otherwise, Claude Code should pick up changes in skill directories automatically.

## Install For Claude.ai

Claude.ai custom skills are uploaded as a ZIP file. Create a ZIP whose root folder is the skill folder:

```bash
tmpdir=$(mktemp -d)
git clone https://github.com/syzkillall/comprehensive-thinking-skill.git "$tmpdir/comprehensive-thinking"
cd "$tmpdir"
zip -r comprehensive-thinking.zip comprehensive-thinking
```

Then upload `comprehensive-thinking.zip` in Claude.ai:

```text
Claude.ai -> Settings / Customize -> Skills -> Add custom skill
```

After uploading, enable the skill and test it with a prompt that should trigger comprehensive thinking.

## Test Prompt

Use this prompt in Codex, Claude Code, or Claude.ai:

```text
请用全面思考帮我判断：这个复杂问题应该怎么理解？
```

The assistant should recognize `全面思考` / `comprehensive-thinking` as the skill trigger and use the five-review reasoning workflow from `SKILL.md`.

## Update

If you installed with `git clone`, update with:

```bash
cd ~/.codex/skills/comprehensive-thinking
git pull
```

For Claude Code personal install:

```bash
cd ~/.claude/skills/comprehensive-thinking
git pull
```

Restart the relevant app after updating if it does not detect the change automatically.

## Uninstall

Codex:

```bash
rm -rf ~/.codex/skills/comprehensive-thinking
```

Claude Code personal install:

```bash
rm -rf ~/.claude/skills/comprehensive-thinking
```

For Claude.ai, remove or disable the skill from the Skills settings page.

## Files Installed

The skill folder contains:

```text
SKILL.md
agents/openai.yaml
references/master-theory-research.md
examples/prompts.md
evals/quality-checklist.md
```

`SKILL.md` is the required runtime file. The other files provide UI metadata, reference material, examples, and quality checks.
