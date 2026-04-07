# Product Brief

## Product Name
Tech Marketing Framework

## One Line Description
A Claude Code project that turns your terminal into a marketing workbench for developer tools companies, with 9 skills, 3 agents, and autonomous skill optimization.

## Problem Statement
Marketing teams at developer tools companies produce content that sounds like generic SaaS marketing. The output reads like it was written by someone who has never shipped code. The tools they use (Jasper, Copy.ai, Writer) are browser based, disconnected from the codebase, and optimized for volume marketers writing about consumer products. They have no awareness of the product brief, no understanding of technical audiences, and no way to enforce voice and quality standards across assets.

The result: developers ignore the content, trust erodes, and launch momentum stalls.

Technical PMMs and founding marketers at dev tools companies need a content generation system that lives where they work (the terminal), reads the product context automatically, and enforces opinionated writing standards tuned for technical audiences.

## Key Capabilities

| Skill | What It Does |
|-------|-------------|
| `/messaging-positioning` | Interactive Socratic workshop that builds the messaging and positioning doc through structured Q&A |
| `/social-posts` | Generates LinkedIn and Twitter posts (brand or personal) from source content |
| `/email` | Generates event follow-up email sequences (4 emails, programmatic personalization) |
| `/ads` | Generates paid ad copy for Google, Meta, and LinkedIn using a creative matrix (Topics x Personas x Angles) |
| `/sales-deck` | Creates B2B sales narrative decks using April Dunford's 8-step methodology |
| `/blog` | Generates SEO/AEO optimized blog posts with tri-publish variants (website, LinkedIn Pulse, X articles) |
| `/image` | Generates marketing images via MCP server, reads brand guidelines for consistency |
| `/skill-builder` | Meta-skill for designing and creating new skills or agents |
| `/autoresearch` | Autonomous skill optimization via binary evals (based on Andrej Karpathy's autoresearch methodology) |

| Agent | What It Does |
|-------|-------------|
| `asset-reviewer` | Reviews any generated asset against content guidelines, product brief, and messaging positioning |
| `ads-auditor` | Analyzes ad campaign performance with health scoring and optimization recommendations |
| `how-they-market` | Analyzes how a company, person, or newsletter markets themselves across channels |

### How It Works
1. Clone the repo into your project or use standalone
2. Fill in `/docs/inputs/` with your product brief, personas, competitive intel, and messaging
3. Run Claude Code. It adopts the marketing persona and loads all context automatically.
4. Use slash commands to generate assets. Every skill reads the docs before generating.
5. Run the asset reviewer agent on any output to enforce quality standards.

### Architecture Decisions
- **CLAUDE.md as identity**: The core personality, voice guidelines, and workflow rules live in `claude.md`, which Claude Code loads automatically. This means every interaction inherits the marketing persona without prompting.
- **Rules as guardrails**: Content guidelines (banned words, structural anti-patterns, AI discoverability rules) live in `.claude/rules/` and apply to every skill output.
- **Docs as context**: Product briefs, personas, and competitive intel live in `/docs/inputs/` and get read by every skill before generating. The content is always grounded in real product data.
- **Skills as workflows**: Each skill is a standalone SKILL.md that defines inputs, steps, rules, and output format. Skills are composable (blog skill hands off to social-posts skill for promotion).
- **Autoresearch for optimization**: Skills improve themselves through autonomous eval loops. Define pass/fail criteria, run the skill repeatedly, score outputs, mutate the prompt, keep improvements.

## Processing Modes / Tiers
Not applicable. This is a free, open-source project. All capabilities are available to anyone with Claude Code installed.

## Limitations
- Requires a Claude Code subscription (Claude Pro, Team, or Enterprise)
- Content quality depends on the quality of the product docs filled in by the user
- Image generation requires the `mcp-image` MCP server to be configured
- Autoresearch consumes significant token volume during optimization runs
- Skills generate drafts, not final copy. Human review is required.
- No GUI. Terminal only. This is a feature for the target audience, not a bug.

## Existing Customers Using This
- Jing Reyhan (VP Marketing) uses this daily as a personal marketing workbench
- Internal team adoption [OPEN: get specific team member usage details]

## Links
- GitHub: https://github.com/j1ngg/tech-marketing-framework
- License: MIT
- Prerequisites: Claude Code CLI (`npm install -g @anthropic-ai/claude-code`)
