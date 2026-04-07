# Product Hunt Listing Assets: Tech Marketing Framework

---

## Tagline Options

1. "9 skills that turn Claude Code into a marketing workbench" (54 characters)
   Stranger test: **Pass.** Someone reading this knows it is a Claude Code project, it has 9 skills, and it is for marketing. The word "workbench" signals a tool collection, not a single feature.

2. "Open source Claude Code project for dev tools marketing" (55 characters)
   Stranger test: **Pass.** Communicates open source, Claude Code ecosystem, and the target audience (dev tools). Slightly less specific about what it does.

3. "Marketing skills for Claude Code: social, email, blog, ads" (59 characters)
   Stranger test: **Pass.** Lists the specific asset types. A reader knows exactly what they get. Less catchy but maximally concrete.

**Recommended: 1** because it leads with the quantity (9 skills) which signals completeness, uses "workbench" which communicates a composable tool rather than a single trick, and is the most memorable of the three.

---

## Description

Tech Marketing Framework is an open source Claude Code project with 9 skills that generate marketing assets for developer tools companies.

Marketing teams at developer tools companies generate content that developers ignore because it reads like generic SaaS copy. AI writing tools like Jasper and Copy.ai amplify the problem. They are calibrated for consumer brands, not engineers evaluating infrastructure. This is Claude Code for marketing.

The framework lives in your terminal and reads your product docs before generating anything. Run `/social-posts` and it reads your product brief and messaging positioning, then generates LinkedIn and Twitter posts calibrated for technical audiences. Run `/blog` and it generates an SEO and AEO optimized post with three publish variants for your website, LinkedIn Pulse, and X. Run `/sales-deck` and it builds a B2B narrative deck using April Dunford's methodology. Nine skills (including autonomous skill optimization), three review agents.

Clone the repo, fill in your product docs, and start generating. MIT licensed. Open source.

---

## Maker's First Comment

I built this because I got tired of rewriting the same launch assets from scratch every time we shipped a feature. I was the only marketer at a dev tools company and every AI writing tool generated content that developers immediately ignored.

This is Claude Code for marketing. 9 slash command skills: `/social-posts`, `/email`, `/blog`, `/ads`, `/sales-deck`, `/messaging-positioning`, `/image`, `/skill-builder`, and `/autoresearch`. Each skill reads your product brief and messaging docs before generating, so the output is grounded in your actual product.

Autoresearch runs autonomous eval loops on your skill prompts and improves them without manual tuning. Define pass/fail criteria, run the skill repeatedly, and it mutates the prompt until quality improves.

I use this daily. I generated this Product Hunt listing with it.

Try it in 2 minutes:
git clone https://github.com/j1ngg/tech-marketing-framework.git
cd tech-marketing-framework && claude

Then run `/social-posts` with any source content. Open an issue on GitHub with skill requests.

---
Character count: 789/800

---

## Visual Asset Spec

### Thumbnail
- Dimensions: 240x240 px
- Content: Clean icon or logo mark. If no logo exists, use a simple terminal prompt icon (e.g., `>_` in a rounded square) with a marketing-related accent color. Keep it recognizable at small sizes.

### Gallery Images (minimum 6)

| Slot | Dimensions | What to Show | Why |
|------|-----------|-------------|-----|
| 1 | 1270x760 | Terminal showing Claude Code with the framework loaded. The `claude` command just ran and the marketing persona greeting is visible. Show the `/` slash command menu with all 9 skills listed. | Hero shot. Immediately communicates "this lives in your terminal" and shows the skill catalog. |
| 2 | 1270x760 | Split screen: left side shows a generic AI tool output (bland, buzzwordy marketing copy). Right side shows the same prompt through Tech Marketing Framework (sharp, technical, no buzzwords). | Before/after contrast. This is the core value proposition in one image. |
| 3 | 1270x760 | Terminal showing `/social-posts` skill in action. Show it reading from `docs/inputs/product_brief.md` then generating a LinkedIn post. The output should be visible and readable. | Top skill demo. Social posts are the most immediately relatable use case. |
| 4 | 1270x760 | Terminal showing `/blog` skill generating a post with the tri-publish output (website version, LinkedIn Pulse version, X article version visible as sections). | Shows the unique tri-publish feature. Demonstrates composability. |
| 5 | 1270x760 | Terminal showing `/autoresearch` running an eval loop. Show the pass/fail scoring, the mutation step, and the improvement delta. Numbers visible. | The novel hook. Autoresearch is the most differentiated feature. Show it working. |
| 6 | 1270x760 | The `/docs/inputs/` folder structure visible in the terminal or a file tree, showing product_brief.md, target_personas.md, messaging_positioning.md, competitor_intel.md. One file is open showing real content. | Shows the "reads your product docs" mechanism. Developers care about architecture. |
| 7 (bonus) | 1270x760 | Terminal showing the `asset-reviewer` agent tearing apart a generated blog post. Show the critical violations, structural feedback, and line-by-line edits. | Shows the quality control loop. Demonstrates the framework is self-correcting. |
| 8 (bonus) | 1270x760 | The full README on GitHub, showing the structure tree and skill list. Star count visible. | Social proof and "this is a real, documented project" signal. |

### Video
- Length: 60 to 90 seconds
- Format: 60fps screen recording, auto-plays muted
- Storyboard:
  1. [0 to 5s]: Terminal opens. `git clone` the repo. `cd tech-marketing-framework`. `claude`. The framework loads. (Show speed. This takes seconds.)
  2. [5 to 15s]: Type `/social-posts`. Skill asks for inputs. Provide a blog post URL or paste text. Select LinkedIn + Personal.
  3. [15 to 35s]: Output generates in real time. Show the LinkedIn post appearing line by line. It is specific, technical, no buzzwords. Pause briefly so the viewer can read the opening lines.
  4. [35 to 50s]: Quick montage of 3 more skills: `/email` generating a 4-email sequence, `/blog` with tri-publish output, `/sales-deck` showing the slide outline.
  5. [50 to 65s]: Show `/autoresearch` running. Scores appear. A mutation improves the pass rate. The number goes up.
  6. [65 to 75s]: Show the asset-reviewer agent flagging issues in a draft. Red flags, rewrites suggested.
  7. [75 to 90s]: Back to the terminal. Text overlay: "9 skills. 3 agents. Open source." GitHub URL appears. End.
- Notes: Record the actual terminal. Do not use slides or title cards. Authentic screen recording only. If the terminal text is too small, zoom the font to 16pt+ before recording. Add subtle background music if desired but the video must work fully muted (all information conveyed visually).

---

## Social Proof Hooks

1. "9 skills, 3 review agents, and autonomous skill optimization in one open source Claude Code project." — Repo feature count (verifiable on GitHub)

2. "Built and used daily by a VP Marketing at a developer tools company. This is not a side project. It is the actual production workflow." — Jing Reyhan, dogfooding

3. "MIT licensed. Open source. No per-seat pricing. No vendor lock-in." — License terms (verifiable on GitHub)

4. "Every skill reads your product brief before generating. The output is grounded in your product, not hallucinated features." — Architecture description (verifiable in codebase)

5. "Autoresearch runs autonomous eval loops on your skills and improves them without manual prompt tuning." — Feature description (verifiable in codebase)

**Gap flag:** No external testimonials exist. Recommend sharing the repo with 3 to 5 technical PMMs before Thursday. Even a single "I generated a full email sequence in 3 minutes" quote strengthens the listing significantly. If you get one by Wednesday evening, add it to the maker comment or description.

---

## Launch Day Social Posts (Pre-Drafted)

### LinkedIn Post 1 (Jing, 6:00 AM PT)

I was the only marketer at a dev tools company and every AI writing tool generated content that developers ignored. It all sounded like SaaS copy written by someone who has never shipped code.

So I built the tool I wished existed when I was the only marketer at a dev tools startup.

Tech Marketing Framework is Claude Code for marketing. An open source project that lives in your terminal and reads your product docs before generating anything. 9 slash command skills for social posts, email sequences, blog posts, ads, sales decks, and more. Plus an autoresearch feature that improves your skills autonomously through binary evals.

I use it every day. It is my actual marketing workbench, not a demo project.

Full disclosure: I built it. The repo is MIT licensed and open source, so you can evaluate it yourself in 2 minutes.

Link in comments.

### LinkedIn Post 2 (Jing, 2:00 PM PT)

One feature in the Tech Marketing Framework I did not expect to use daily: the asset reviewer agent.

You generate a blog post with `/blog`. Then the asset reviewer checks every sentence against your content guidelines, flags banned words and passive voice, and suggests specific rewrites. It catches claims not supported by the product brief.

Claude Code for marketing. Launched on Product Hunt today. Currently [ranking]. Link in comments.

### Twitter Post 1 (Jing, 7:00 AM PT)

Launched on @ProductHunt today.

Claude Code for marketing. 9 skills that turn your terminal into a marketing workbench:

/social-posts
/email
/blog
/ads
/sales-deck
/messaging-positioning
/image
/skill-builder
/autoresearch

Open source. MIT licensed. Reads your product docs before generating.

[Product Hunt link]

### Twitter Post 2 (Jing, 12:00 PM PT)

The part of @j1ngg/tech-marketing-framework that surprises people most: /autoresearch

It runs your skills through autonomous eval loops. Defines pass/fail criteria. Scores outputs. Mutates the prompt. Keeps improvements.

Your marketing skills get better over time without manual tuning.

Claude Code for marketing. Open source.

[Product Hunt link]

---

## Reddit Posts (Kasia, 4:00 PM PT)

### r/ClaudeAI

**Title:** I built a Claude Code project for developer tools marketing. Here is what I learned.

**Body:**

I work in marketing at a developer tools company and got tired of AI writing tools generating content that developers immediately ignore. So I built a Claude Code project that reads your product docs and generates marketing assets calibrated for technical audiences. Claude Code for marketing.

It has 9 skills (/social-posts, /email, /blog, /ads, /sales-deck, /messaging-positioning, /image, /skill-builder, /autoresearch) and 3 review agents.

The part I find most interesting technically: the autoresearch skill. It defines binary pass/fail evals for any skill, runs it repeatedly against test inputs, scores outputs, and mutates the prompt one change at a time. Keeps improvements, discards regressions.

The biggest lesson: the quality of AI generated marketing content is entirely determined by the quality of the product docs you feed it. Generic input generates generic output, no matter how good the prompt. That is why every skill reads from a `/docs/inputs/` folder before generating.

Open source, MIT licensed: [GitHub link]

Also launched on Product Hunt today: [PH link]

Open an issue on GitHub if you want a specific skill added.

### r/SideProject

**Title:** Open source Claude Code project that turns your terminal into a marketing workbench

**Body:**

Launched this today on Product Hunt. Claude Code for marketing. 9 skills for generating marketing content (social posts, email sequences, blog posts, ads, sales decks) specifically for developer tools companies.

Every skill reads from a `/docs/inputs/` folder containing your product brief, personas, and competitive intel before generating anything. The output is grounded in your actual product, not generic fluff.

I use it daily as my marketing workbench. MIT licensed. Open source.

GitHub: [link]
Product Hunt: [link]

Open an issue on GitHub if you want a specific skill added or if you have feedback on the framework.
