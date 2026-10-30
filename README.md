# Claude Skills by elhuzain

Skills for [Claude Code](https://claude.com/claude-code) that help build calm, editorial websites with Next.js. Install only the ones you need.

## Skills

### frontend-architectural-design

Gives any website the look of an architecture studio's portfolio: light, oversized headings, generous whitespace, sharp corners, large imagery and a near-monochrome palette. Claude applies the rules to every section it builds and starts from ready-made Tailwind CSS v4 templates: a full design system stylesheet, a hero, feature cards and a project grid.

### gsap-scroll-animations

Adds smooth scrolling, scroll-triggered reveals, image wipes and parallax to a Next.js site in minutes, without turning your sections into client components. Elements are animated with simple `data-animate` attributes, and the skill includes templates for the whole setup plus a reversible menu animation.

The two skills work well together: design first, then add motion.

## Install

In a Claude Code session, add the marketplace once:

```text
/plugin marketplace add elhuzain/claude-skills
```

Then install the skill you want:

```text
/plugin install frontend-architectural-design@elhuzain-skills
/plugin install gsap-scroll-animations@elhuzain-skills
```

Or browse everything with `/plugin`.

From a regular terminal, the same commands are:

```bash
claude plugin marketplace add elhuzain/claude-skills
claude plugin install gsap-scroll-animations@elhuzain-skills
```

## Update

```bash
claude plugin marketplace update elhuzain-skills
claude plugin update gsap-scroll-animations@elhuzain-skills
```

Restart Claude Code to apply an update.

## Use

Skills load automatically when relevant. For example:

- "Style the hero section" or "Create a services section" uses **frontend-architectural-design**.
- "Add smooth scrolling" or "Animate the sections on scroll" uses **gsap-scroll-animations**.

## Structure

```text
.claude-plugin/marketplace.json        catalog of all skills
plugins/<name>/.claude-plugin/plugin.json
plugins/<name>/skills/<name>/SKILL.md  the skill itself, plus templates/
```

## Author

Built by [elhuzain](https://elhuzain.com).
