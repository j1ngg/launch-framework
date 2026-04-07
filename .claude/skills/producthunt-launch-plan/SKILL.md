---
name: producthunt-launch-plan
description: Interactive planning skill that produces a dated Product Hunt launch checklist with workstreams, asset inventory, outreach cadence, team roles, and launch day runsheet.
autoload: false
---

# Product Hunt Launch Planner

This skill produces a complete, dated launch plan for a developer tool on Product Hunt. It asks questions, captures answers, and outputs an actionable checklist.

## Step 1: Gather Launch Parameters

Before building the plan, ask the user these questions. Wait for answers before proceeding. Do not assume.

### Launch Basics

1. **What is the product?** (Name and one-sentence description)
2. **What is the target launch date?** (PH day runs 12:01 AM to 11:59 PM Pacific Time. Wednesdays and Tuesdays perform best. 2nd or 3rd week of month for monthly badge potential.)
3. **Is this the initial product launch or a feature update?**
4. **Is the product open source?**

### Team and Resources

5. **Who is the maker?** (The person whose PH account will post. Must be a personal account, not a company account.)
6. **Who else is on the launch team?** (Names and roles. Need at minimum: maker, outreach lead, social lead. Ideally also a community lead.)
7. **Does the team have timezone coverage for a full 24-hour launch day?** (Need coverage for 12 AM to 11:59 PM PT at minimum.)

### Existing Assets

8. **Do you have an existing email list? How large?**
9. **Do you have an active community (Discord, Slack, etc.)? How many members?**
10. **Do you have existing Product Hunt accounts with 6+ months of activity?** (How many team members?)
11. **Do any team members have existing PH follower bases?**
12. **Do you have a demo, playground, or sandbox that requires no signup?**

### Hunter Decision

13. **Do you want to self-hunt or pursue a third-party hunter?** (Self-hunting gives full control. Top-500 hunters get 3.2x more upvotes but require outreach 6 weeks out. See `docs/producthunt_playbook.md` for hunter strategy.)

---

## Step 2: Build the Plan

Once all questions are answered, read `docs/producthunt_playbook.md` for reference data, then generate the full plan below.

Calculate all dates backwards from the target launch date. Use absolute dates (e.g., "Monday, May 12") not relative dates (e.g., "6 weeks out").

---

### Output Format

```markdown
# Product Hunt Launch Plan: [Product Name]

**Launch date:** [Day, Date] (Pacific Time)
**Maker:** [Name]
**Hunter:** [Self / Name]
**Goal:** [Product of the Day / Top 5 / Featured]

---

## Pre-Launch Readiness

### Gaps to Close Before Committing to Launch Date

[List any critical gaps identified from Step 1 answers. Examples:]
- [ ] No zero-friction demo exists (top PH listings link to something visitors can try immediately)
- [ ] No team members have aged PH accounts (need 6+ months of activity for 10x vote weight)
- [ ] No email list (target 300 to 500 committed supporters minimum)
- [ ] No testimonials secured (playbook rule: testimonials are mandatory)

If any gaps are critical, recommend the user address them before committing to the launch date.

---

## Timeline: [calculated start date] to [launch date]

### Phase 1: Foundation ([6 weeks out date] to [4 weeks out date])

**PH Account Warming**
- [ ] [Date]: All team members create PH accounts (if not existing)
- [ ] [Date range]: Team engages daily on PH (upvote, comment on 2 to 3 products per day)
- [ ] [Date range]: Maker follows relevant makers and communities on PH

**Hunter Outreach** (if pursuing third-party hunter)
- [ ] [Date]: Identify 5 to 10 candidate hunters in dev tools category
- [ ] [Date range]: Engage with candidates' content (comment on posts, support products they hunt)
- [ ] [Date]: Send hunter outreach DM (template in playbook)
- [ ] [Date]: Provide hunter with early product access
- [ ] [Date]: Confirm hunter commitment and share draft assets

**Supporter List Building**
- [ ] [Date]: Start monitoring [hunted.space](https://hunted.space) for category benchmarks
- [ ] [Date]: Begin identifying Tier 1 supporters (PH veterans with 6+ month accounts)
- [ ] [Date]: Set up outreach tracking spreadsheet (contact, channel, commitment, follow up status)

**Owner:** [Name]

---

### Phase 2: Outreach and Assets ([4 weeks out date] to [2 weeks out date])

**Supporter Outreach**
- [ ] [Date]: Email list Wave 1: explain PH, ask subscribers to create accounts (template in playbook)
- [ ] [Date range]: Begin warm outreach to Tier 1 supporters via LinkedIn DMs (template in playbook)
- [ ] [Date]: Target: 100+ committed supporters identified
- [ ] [Date]: Email list Wave 2: ask subscribers to upvote/comment on 2 to 3 products to warm accounts (template in playbook)

**Asset Creation**
- [ ] [Date]: Run `/producthunt-listing` skill to generate: tagline, description, maker comment, visual spec, social proof hooks
- [ ] [Date]: Run asset reviewer agent on listing output
- [ ] [Date]: Begin visual asset production (screenshots, video) per visual asset spec
- [ ] [Date]: Draft 3 tagline versions and test with 5 beta users
- [ ] [Date]: Finalize tagline based on stranger test results

**Cross-Promotion**
- [ ] [Date]: Identify 5 to 10 companies for mutual launch agreements
- [ ] [Date range]: Support their launches with genuine comments and upvotes
- [ ] [Date]: Reach out to propose mutual support arrangement

**Owner:** [Name]

---

### Phase 3: Final Prep ([2 weeks out date] to [5 days out date])

**Listing Finalization**
- [ ] [Date]: Write maker's first comment (final version)
- [ ] [Date]: Complete all visual assets (minimum 6 gallery images + video)
- [ ] [Date]: Set PH teaser page live
- [ ] [Date]: Ask Tier 1 supporters to click "Notify Me" (template in playbook)

**Launch Kit**
- [ ] [Date]: Prepare launch kit for supporters containing:
  - 2 to 3 pre-written social posts (LinkedIn, Twitter, generic)
  - Product screenshots formatted for social sharing
  - 3-bullet summary of what the product does
  - Product Hunt link
  - One sentence copy-paste for PH comments
- [ ] [Date]: Distribute launch kit to all committed supporters

**Social Content**
- [ ] [Date]: Run `/social-posts` skill with PH listing as source to generate launch day posts
- [ ] [Date]: Pre-draft LinkedIn posts for launch day (3 to 5 posts, link always in comment not body)
- [ ] [Date]: Pre-draft Twitter posts for launch day
- [ ] [Date]: Pre-draft email waves (3 waves, see playbook for timing)

**Owner:** [Name]

---

### Phase 4: Final 5 Days ([5 days out date] to [day before launch])

- [ ] [Date]: Personal outreach to top 20 contacts (phone, text, voice)
- [ ] [Date]: Final review of all listing assets
- [ ] [Date]: Test all links in the listing
- [ ] [Date]: Brief supporters with launch kit and launch day timing
- [ ] [Date]: Confirm team roles and timezone coverage for launch day
- [ ] [Date]: Final rehearsal: maker posts first comment draft, team reviews

**Owner:** [Name]

---

## Launch Day Runsheet: [Launch Date]

| Time (PT) | Action | Owner | Details |
|-----------|--------|-------|---------|
| 12:01 AM | Go live | Maker | Post maker comment (written 48 hours prior) |
| 12:05 AM | Activate core team | Outreach lead | Slack/Discord DMs to most committed supporters |
| 1:00 AM | Email Wave 1 | Outreach lead | 15 to 20% of list (most engaged segment) |
| 4:00 AM | European wave | Outreach lead | Direct messages to European contacts |
| 6:00 AM | Social post 1 | Social lead | Founder LinkedIn post (personal story, link in comment) |
| 8:00 AM | Email Wave 2 | Outreach lead | Main blast, 40 to 50% of list |
| 8:00 AM | Social post 2 | Social lead | Twitter/X announcement |
| 9 AM to 12 PM | Comment engagement | Maker | Reply to every PH comment within 5 to 9 minutes |
| 10:00 AM | Network leverage | Social lead | Ask friendly founders to mention in standups |
| 12:00 PM | Social post 3 | Social lead | Mid-day milestone update with ranking |
| 1:00 PM | Metrics review | Maker | Check bounce rates. Adjust landing page if >55 to 60%. |
| 4:00 PM | Email Wave 3 | Outreach lead | Plain text follow up to non-openers |
| 6:00 PM | Social post 4 | Social lead | Final push, 2 to 3 hours before close |
| 8:00 PM | Transparent update | Social lead | Post ranking with final CTA |
| 11:59 PM | Transition | Maker | Screenshot final ranking. Begin post-launch sequence. |

### Team Roles

| Role | Person | Timezone | Responsibility |
|------|--------|----------|---------------|
| Maker | [Name] | [TZ] | Post maker comment, respond to all PH comments, social posts |
| Outreach lead | [Name] | [TZ] | Manage email waves, DM supporters, timezone coordination |
| Social lead | [Name] | [TZ] | LinkedIn/Twitter posts and engagement throughout day |
| Community lead | [Name] | [TZ] | Activate Discord/Slack, monitor Reddit |

---

## Post-Launch Plan: [Launch Date + 1] to [Launch Date + 30]

| Day | Action | Owner |
|-----|--------|-------|
| Day 1 | Thank-you post and launch recap on social | Social lead |
| Day 1 | Respond to every remaining PH comment | Maker |
| Day 0 to 2 | Welcome emails to PH visitors, dedicated onboarding path | [Name] |
| Day 3 | Tutorial or quick-start guide published | [Name] |
| Day 3 | Extract emails from engaged PH commenters | Outreach lead |
| Day 7 | Case study or early win story | [Name] |
| Day 7 | Follow up with journalists who covered launch | Social lead |
| Day 14 | Early access offer or discount for PH community | [Name] |
| Day 3 to 30 | Self-serve: onboarding optimization, upgrade prompts | [Name] |
| Day 3 to 30 | Sales-assisted: lead capture, demo loop, pilot offers | [Name] |
| Day 30 | Internal retrospective: what worked, what to change for next launch | All |

---

## Asset Inventory

| Asset | Status | Owner | Due Date | Reviewer |
|-------|--------|-------|----------|----------|
| PH tagline (3 options, tested) | [ ] | | | |
| PH description | [ ] | | | |
| Maker's first comment | [ ] | | | |
| Gallery images (6+ at 1270x760) | [ ] | | | |
| Product video (60 to 90s) | [ ] | | | |
| Thumbnail (240x240) | [ ] | | | |
| Launch kit for supporters | [ ] | | | |
| LinkedIn posts (3 to 5 pre-drafted) | [ ] | | | |
| Twitter posts (pre-drafted) | [ ] | | | |
| Email Wave 1 (most engaged, 15 to 20%) | [ ] | | | |
| Email Wave 2 (main blast, 40 to 50%) | [ ] | | | |
| Email Wave 3 (follow up, non-openers) | [ ] | | | |
| Dedicated PH onboarding path | [ ] | | | |
| Zero-friction demo/playground | [ ] | | | |
| Welcome email for PH visitors | [ ] | | | |

---

## Success Metrics

| Metric | Target (Featured) | Target (Not Featured) |
|--------|-------------------|----------------------|
| Upvotes | 500+ | 100+ |
| Comments | 50+ genuine | 15+ |
| Visitors | 1,000 to 5,000 | 100 to 500 |
| Signups | 10 to 150 | 1 to 15 |
| Visitor to signup rate | 15 to 25% | 10 to 15% |
| Result | Product of the Day | Featured |

---

## Multi-Launch Note

Product Hunt rewards compounding. Each launch adds followers who get notified of the next one. After this launch, identify the next major feature milestone that qualifies for a separate launch. Only launch for: major feature releases, new platform/integration support, or significant version milestones. Do not launch for bug fixes, UI refreshes, or minor improvements.
```

---

## Step 3: Review and Adjust

After generating the plan, ask the user:

1. "Are the team role assignments correct?"
2. "Are there any dates that conflict with holidays, company events, or other launches?"
3. "Do you want to adjust the goal (Product of the Day vs Featured vs Top 5)?"

Make adjustments based on their answers and output the final plan.

Save the final plan to `output/producthunt_launch_plan.md`.
