---
name: producthunt-listing
description: Generates Product Hunt listing assets for developer tool launches. Produces tagline options, description, maker comment, visual asset spec, and social proof hooks.
autoload: false
---

# Product Hunt Listing Generator

This skill generates the complete set of Product Hunt listing assets for a developer tool launch.

## Step 1: Gather Context

Before generating any assets, read the following project docs:

1. `docs/product_brief.md` for product capabilities and limitations
2. `docs/messaging_positioning.md` for core positioning and value props
3. `docs/target_personas.md` for ICP definitions
4. `docs/competitor_intel.md` for competitive landscape
5. `docs/producthunt_playbook.md` for PH-specific best practices

Then ask the user:

**What is the launch context?**
- Is this the initial product launch or a major feature update?
- If a feature update: what specifically is new?
- Is the product open source?

**Who is the maker?**
- Name and role of the person posting
- Personal connection to the problem (for the maker comment)
- Any existing adoption metrics to reference (users, downloads, stars)

**What is the zero-friction CTA?**
- Live demo URL, playground, or sandbox (no signup required)
- If none exists, flag this as a gap. Top PH listings link to something the visitor can try immediately.

Wait for the user to answer before proceeding.

---

## Step 2: Generate Listing Assets

Generate all assets below in a single output. Follow every rule precisely.

---

### Asset 1: Tagline Options (3 Variants)

Generate exactly three tagline options. Each must be under 60 characters.

**Rules for developer tool taglines:**
- Feature-first beats benefit-first. Developers parse feature statements faster than value propositions.
- If the product is open source, lead with that. "The open-source [known brand] alternative" formula consistently wins (#1 Month for Appwrite Sites).
- If the product can be compared to a known tool, use the "[Product] for [category]" formula (Chronicle won with "Cursor for Slides").
- The tagline must answer "What is this?" for someone who has never heard of the product.
- No buzzwords (robust, seamless, revolutionary, cutting-edge, AI-powered).
- No vague benefit language ("boost productivity", "streamline workflows").

**Validation test:** State after each tagline whether a stranger could repeat back what the product does after reading it. If no, flag for revision.

**Output format:**

```
## Tagline Options

1. "[tagline]" ([character count])
   Stranger test: [pass/fail + reasoning]

2. "[tagline]" ([character count])
   Stranger test: [pass/fail + reasoning]

3. "[tagline]" ([character count])
   Stranger test: [pass/fail + reasoning]

Recommended: [number] because [reasoning]
```

---

### Asset 2: Description

2 to 3 paragraphs. Lead with the problem, not the solution.

**Structure:**
1. Opening hook: one sentence that names the specific pain. Use a concrete number or scenario. ("Your team spends 30 minutes daily re-explaining decisions in Slack.")
2. What you built: one to two sentences describing what the product does in plain language.
3. How it works: one to two sentences on the mechanism. Include a technical detail that signals credibility to developers.
4. What makes it different: one sentence on the specific differentiator that no alternative offers. Pull from the differentiated value map in `docs/messaging_positioning.md`.

**Rules:**
- No dashes of any kind
- No passive voice
- No banned words from content guidelines
- No claims not supported by `docs/product_brief.md`
- Keep paragraphs under 80 words each

---

### Asset 3: Maker's First Comment (Under 800 Characters)

This comment is weighted heavily by the PH algorithm. One quality comment ≈ 40 to 50 upvotes.

**Structure:**
1. The problem and personal motivation (1 to 2 sentences)
2. What is new or what changed (1 sentence)
3. One concrete use case developers will recognize (1 sentence)
4. Zero-friction CTA (1 sentence with link)
5. Specific feedback ask (1 sentence)

**Rules:**
- Under 800 characters total. Count and display the character count.
- First person voice from the maker
- No hype language
- No roadmap promises
- Anchor in user demand or adoption metrics if available
- The CTA must link to something that requires no signup

**Output format:**

```
## Maker's First Comment

[Comment text]

---
Character count: [X]/800
```

---

### Asset 4: Visual Asset Spec

Generate a shot list for the PH gallery based on the product's actual capabilities.

**Required format:**

```
## Visual Asset Spec

### Thumbnail
- Dimensions: 240x240 px
- Content: [specific recommendation based on the product]

### Gallery Images (minimum 6)

| Slot | Dimensions | What to Show | Why |
|------|-----------|-------------|-----|
| 1 | 1270x760 | [specific screen/feature] | Hero shot, first impression |
| 2 | 1270x760 | [specific before/after] | Problem → solution contrast |
| 3 | 1270x760 | [specific feature] | Top capability |
| 4 | 1270x760 | [specific feature] | Second capability |
| 5 | 1270x760 | [specific output/result] | Proof it works (not just config) |
| 6 | 1270x760 | [specific workflow/integration] | Real-world context |

### Video
- Length: 60 to 90 seconds
- Format: 60fps, auto-plays muted
- Storyboard:
  1. [0 to 5s]: [specific visual hook, no title cards]
  2. [5 to 20s]: [specific problem demonstration]
  3. [20 to 50s]: [specific product solving the problem]
  4. [50 to 70s]: [specific result/output]
  5. [70 to 90s]: [CTA with URL]
- Notes: Skip cinematic production. Authentic screen recordings outperform polished videos. First 5 seconds must hook visually (video auto-plays muted).
```

Tailor every slot to the specific product. Do not use generic placeholders like "Feature A" or "Key benefit." Name the actual screen, feature, or workflow based on the product brief.

---

### Asset 5: Social Proof Hooks

Generate 3 to 5 proof points that can be used across the listing, social posts, and launch kit.

**Pull from:**
- `docs/testimonials.md` for customer quotes
- `docs/product_brief.md` for adoption metrics
- GitHub stars, download counts, or integration stats if available

**Format each as a standalone one-liner:**

```
## Social Proof Hooks

1. "[proof point]" — [source/attribution]
2. "[proof point]" — [source/attribution]
3. "[proof point]" — [source/attribution]
```

If no testimonials or metrics exist, flag this as a gap and recommend the user secure at least one before launch. Reference the playbook rule: "Testimonials are mandatory."

---

## Review Checklist (Self-Check Before Delivery)

Before delivering, verify every asset against:

- [ ] All taglines under 60 characters
- [ ] No dashes in any asset
- [ ] No passive voice
- [ ] No banned words or phrases from content guidelines
- [ ] No claims unsupported by product brief
- [ ] Maker comment under 800 characters
- [ ] Maker comment includes zero-friction CTA
- [ ] Visual asset spec references actual product features (no generic placeholders)
- [ ] Description leads with problem, not solution
- [ ] Social proof hooks have attribution

---

## Output Structure

Deliver all five assets in a single response, in order:

1. Tagline Options
2. Description
3. Maker's First Comment
4. Visual Asset Spec
5. Social Proof Hooks

After delivery, ask: "Want me to run the asset reviewer on this output?"
