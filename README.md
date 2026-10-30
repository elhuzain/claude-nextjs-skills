# Claude Skills by elhuzain

Skills for [Claude](https://claude.com) that help build calm, editorial websites with Next.js. Each skill is a self-contained folder: download only the ones you need.

## Skills

| Skill | What it does |
|---|---|
| [`frontend-architectural-design`](frontend-architectural-design) | Gives any website the look of an architecture studio's portfolio: light, oversized headings, generous whitespace, sharp corners, large imagery and a near-monochrome palette. Includes a Tailwind CSS v4 design system and hero, feature card and project grid templates. |
| [`gsap-scroll-animations`](gsap-scroll-animations) | Adds smooth scrolling, scroll-triggered reveals, image wipes and parallax to a Next.js site without turning sections into client components. Elements animate with simple `data-animate` attributes; includes templates for the full setup and a reversible menu animation. |

The two work well together: design first, then add motion.

## Install in Claude Code

Claude Code loads skills from `~/.claude/skills/` (all your projects) or `.claude/skills/` inside a project (that project only, and shared with anyone who clones it).

Download a single skill with one command. Replace `gsap-scroll-animations` with the skill you want.

**Into your personal skills (all projects):**

```bash
mkdir -p ~/.claude/skills && curl -sL https://github.com/elhuzain/claude-skills/archive/refs/heads/main.tar.gz \
  | tar -xz -C ~/.claude/skills --strip-components=1 claude-skills-main/gsap-scroll-animations
```

**Into the current project only:**

```bash
mkdir -p .claude/skills && curl -sL https://github.com/elhuzain/claude-skills/archive/refs/heads/main.tar.gz \
  | tar -xz -C .claude/skills --strip-components=1 claude-skills-main/gsap-scroll-animations
```

**With Node.js installed**, this shorter form does the same:

```bash
npx degit elhuzain/claude-skills/gsap-scroll-animations ~/.claude/skills/gsap-scroll-animations
```

Start a new Claude Code session afterwards. Run the same command again to update a skill to the latest version.

## Install in Claude.ai

1. Download this repo: **Code → Download ZIP**, and extract it.
2. Zip the folder of the skill you want, for example `gsap-scroll-animations/`.
3. In Claude.ai, open **Settings → Capabilities → Skills**, upload the zip and turn the skill on.

## Use

Skills load automatically when relevant. For example:

- "Style the hero section" or "Create a services section" uses **frontend-architectural-design**.
- "Add smooth scrolling" or "Animate the sections on scroll" uses **gsap-scroll-animations**.

## Structure

Each skill is one folder with a `SKILL.md` (instructions Claude reads) and optional `templates/` (code Claude adapts into your project):

```text
<skill-name>/
├── SKILL.md
└── templates/
```

## Author

Built by [elhuzain](https://elhuzain.com).
