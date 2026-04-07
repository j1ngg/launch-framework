# Competitor Intelligence

## Direct Competitors
No tool today combines marketing skill execution with codebase context inside a terminal. The competitive landscape breaks into four buckets, none of which occupy the same intersection.

| Competitor | Positioning | Strengths | Weaknesses | Pricing Model |
|------------|-------------|-----------|------------|---------------|
| Generic Claude Code skill packs (claude-skills, OpenClaudia, ai-marketing-claude) | Collections of Claude Code skills for various use cases | Free, open-source, growing ecosystem | No dev tools specialization. No product context ingestion. No content guidelines. Generic prompts produce generic output. | Free |
| Jasper | Enterprise AI content platform | Large team features, brand voice training, campaign workflows | Browser-based. No codebase awareness. Optimized for consumer/SaaS marketing. $59/mo+ per seat. Developers ignore Jasper-produced content. | $59/mo+ |
| Copy.ai | AI-powered sales and marketing content | Workflow automation, GTM templates | Same problems as Jasper. No technical audience calibration. | $36/mo+ |
| Writer.com | Enterprise AI writing platform with brand governance | Style guides, terminology management, team collaboration | Enterprise pricing. Heavy setup. Not designed for a 1-person marketing team at a Series A dev tools company. | Enterprise |

## Indirect Competitors

| Alternative | How It Works | Why People Use It | Where It Falls Short |
|-------------|-------------|-------------------|---------------------|
| ChatGPT / Claude chat | Copy-paste product context into a chat, ask for marketing copy | Free/cheap, flexible, no setup | No persistent context. Reexplain product every conversation. No quality guardrails. Output drifts between sessions. |
| Manual process (Google Docs + templates) | Write everything from scratch using past launches as templates | Full control, proven | Takes 10x longer. No consistency across assets. Institutional knowledge lives in one person's head. |
| Hire a freelancer or agency | Outsource content to a contractor or marketing agency | Professional output, off-loads execution | Expensive ($5K to $20K per launch). Slow turnaround. Freelancers rarely understand developer audiences. Requires extensive briefing. |
| Doing nothing | Ship the product with a changelog entry and hope developers find it | Zero effort | Zero impact. Launches without marketing support consistently underperform. |

## How We Win
1. **Codebase context**: Skills read `/docs/inputs/` before generating anything. The output is grounded in real product data, not hallucinated features.
2. **Opinionated for dev tools**: Content guidelines ban marketing buzzwords, enforce technical accuracy, and optimize for AI discoverability. This is not a generic writing tool.
3. **Terminal-native**: Lives where technical PMMs and DevRel already work. No context switching to a browser app.
4. **Composable skills**: Blog skill hands off to social-posts skill. Ads skill reads competitive research from how-they-market agent. The pieces connect.
5. **Self-improving**: Autoresearch runs autonomous evals and mutates skill prompts. The framework gets better with use.
6. **Free and open source**: MIT licensed. No per-seat pricing. No vendor lock-in.

## How We Lose
1. **No GUI**: Marketers who live in browser tools will not adopt a terminal workflow. This is a deliberate tradeoff.
2. **Requires Claude Code subscription**: Not truly free. Users need Claude Pro ($20/mo) at minimum.
3. **Setup friction**: Filling in `/docs/inputs/` requires upfront work. Users who skip this step get generic output and blame the tool.
4. **Single-player**: No team collaboration features. No approval workflows. No shared asset library. This is a solo practitioner tool today.
5. **No analytics**: Cannot measure content performance or track what works. Users need separate tools for that.
