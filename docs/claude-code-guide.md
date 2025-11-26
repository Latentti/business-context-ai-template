# Claude Code Guide - AI-Assisted Template Filling

This guide explains how to use the built-in **Business Context Architect** agent to fill your business context template interactively.

## Prerequisites

- [Claude Code](https://claude.ai/claude-code) installed
- This repository cloned locally

## Quick Start

```bash
# 1. Clone the repository
git clone https://github.com/Latentti/business-context-ai-template.git

# 2. Navigate to the repository
cd business-context-ai-template

# 3. Start Claude Code
claude

# 4. Start the guided workflow
/BizContext/start
```

---

## Available Commands

| Command | Description |
|---------|-------------|
| `/BizContext/start` | Start the complete template filling workflow |
| `/BizContext/fill-section` | Fill a specific section interactively |
| `/BizContext/critique` | Evaluate content for AI-usefulness |
| `/BizContext/validate` | Run full document validation |

---

## The Business Context Architect Agent

When you run `/BizContext/start`, you activate the **Business Context Architect** - an AI agent specifically designed to help you create high-quality business context documents.

### What It Does

1. **Guides You Section by Section**
   - Explains what each section is for
   - Asks targeted questions to gather information
   - Tracks your progress

2. **Challenges Vague Content**
   - Immediately flags marketing language
   - Demands specific numbers and evidence
   - Won't accept "we're the best" without proof

3. **Ensures Quality**
   - Every claim needs supporting data
   - No superlatives without metrics
   - Honest gaps are better than false information

4. **Handles Multiple Languages**
   - You can describe your business in any language
   - Agent responds in your language
   - All content written to template is in English

---

## Workflow: `/BizContext/start`

### Step 1: Template Selection

The agent asks which template fits your organization:

```
Which template complexity do you need?

1. Quick Start (4-6 hours) - For startups, small teams (<50 people)
2. Full Template (8-16 hours) - For mid-size companies (50-500 people)
3. Enterprise (16-40 hours) - For large organizations (500+ people)
```

### Step 2: Section-by-Section Filling

For each section, the agent:

1. **Explains the purpose:**
   ```
   Section 1: Executive Summary

   Why AI Needs This:
   Quick overview for AI to understand your business essence.
   AI uses this to calibrate all recommendations.

   Critical Fields:
   - Annual revenue
   - Employee count
   - Customer count
   - Competitive advantage (with evidence)
   ```

2. **Asks questions:**
   ```
   What's your annual revenue?
   (Exact number preferred, range acceptable if private company)
   ```

3. **Challenges vague answers:**
   ```
   ⚠️ NEEDS MORE SPECIFICITY

   You said: "We have many enterprise customers"

   I need:
   - Exact number of enterprise customers
   - Definition of "enterprise" (>1000 employees? >€50M revenue?)
   - Percentage of total customers

   Example:
   ❌ "We have many enterprise customers"
   ✅ "127 enterprise customers (>1000 employees), representing 68% of ARR"

   Please provide specifics:
   ```

### Step 3: Quality Validation

After completing all sections, the agent validates:

```
✅ VALIDATION COMPLETE

Overall Score: 85/100

✓ All required sections filled
✓ No placeholder text
⚠ 2 sections could use more detail
✓ No marketing language detected
✓ Metrics included in key sections

Your document is AI-ready!
```

---

## Example Session

Here's what a typical session looks like:

```
You: /BizContext/start

Agent: 🏗️ Business Context Architect activated!

I'll help you create a business context document that AI tools can actually use.
You can describe your business in any language - I'll write everything in English.

Which template do you need?
1. Quick Start (4-6h)
2. Full Template (8-16h)
3. Enterprise (16-40h)

You: 2

Agent: Great choice! I've created my-business-context.yaml from the Full template.

Let's start with Section 1: Executive Summary.

What's your company name and what do you do in one sentence?

You: Olemme NordicPay, B2B maksujärjestelmä pohjoismaisille verkkokaupoille.

Agent: Got it! Writing in English:
- Company: NordicPay
- Description: B2B payment orchestration for Nordic e-commerce

What's your annual revenue? (Exact or range)

You: Noin 8 miljoonaa euroa

Agent: ⚠️ NEEDS SPECIFICITY

"Around 8 million euros" - can you be more precise?

- Is this ARR (annual recurring revenue)?
- What's the growth rate?
- What year is this for?

You: 8.2M EUR ARR, kasvua 34% viime vuodesta, 2024 ennuste

Agent: ✓ Excellent! Writing:
- Annual Revenue: €8.2M ARR (2024 projected)
- Growth: +34% YoY

Now, how many employees do you have?

[... continues through all sections ...]
```

---

## Language Handling

### Input: Any Language
Describe your business in whatever language is most natural:
- Finnish
- Swedish
- German
- French
- Any other language

### Output: Always English
All content written to the template is in English. This ensures:
- AI development tools work reliably
- Consistent terminology
- Universal accessibility

### Conversation: Your Preference
The agent responds in your language during the conversation.

### Example:
```
You: Meillä on 45 kehittäjää, joista 12 on AWS-sertifioituja

Agent: Hyvä! Kirjoitan templateen:
- Engineering team: 45 developers
- AWS certified: 12

Onko tiimissä muita sertifikaatteja?
```

---

## Fact-Checking: What Gets Challenged

The agent immediately challenges:

### Marketing Language
| You Say | Agent Asks |
|---------|------------|
| "We're the leading provider" | "What's your market share? According to what source?" |
| "Innovative technology" | "What specifically is innovative? How does it differ?" |
| "World-class service" | "What metrics prove this? NPS? Response time? Resolution rate?" |

### Vague Quantities
| You Say | Agent Asks |
|---------|------------|
| "Many customers" | "How many exactly?" |
| "Significant growth" | "What percentage? Over what period?" |
| "Large team" | "How many people? In which functions?" |

### Unverified Claims
| You Say | Agent Asks |
|---------|------------|
| "Customers love us" | "What's your NPS? CSAT? Retention rate?" |
| "High availability" | "What's your uptime SLA? Actual uptime last 12 months?" |
| "Fast performance" | "What's your P99 latency? Under what load?" |

---

## Tips for Best Results

### 1. Have Data Ready
Before starting, gather:
- Financial metrics (revenue, growth, margins)
- Customer metrics (count, segments, NPS)
- Technical details (systems, versions, architecture)
- Team composition (headcount by function)

### 2. Be Honest About Gaps
It's better to say "I don't know" than to guess:
```
You: I don't know our exact market share

Agent: That's fine. I'll note it as:
- Market share: Unknown (consider researching for future update)

Honest gaps are better than false information.
```

### 3. Use Specific Numbers
Instead of ranges, use exact numbers when possible:
```
❌ "50-100 employees"
✅ "67 employees (as of November 2024)"
```

### 4. Include Context
Numbers with context are more useful:
```
❌ "NPS: 72"
✅ "NPS: 72 (industry average: 45, measured quarterly, 2,400 responses)"
```

### 5. Take Breaks
The workflow saves progress automatically. You can:
- Stop anytime and resume later
- Use `/BizContext/fill-section` to work on specific sections
- Complete over multiple sessions

---

## Validation: `/BizContext/validate`

After filling, run validation to check quality:

```
/BizContext/validate
```

The agent checks:
- **Completeness** - All required fields filled
- **Specificity** - Numbers instead of vague terms
- **Factual accuracy** - No marketing language
- **Consistency** - No contradictory information

### Validation Report

```
📋 VALIDATION REPORT

Overall Score: 85/100

| Category | Score | Status |
|----------|-------|--------|
| Completeness | 95/100 | ✅ |
| Specificity | 80/100 | ⚠️ |
| Factual | 90/100 | ✅ |
| Consistency | 75/100 | ⚠️ |

Issues Found:
1. Section 7: Competitor analysis missing win/loss data
2. Section 10: Technology versions incomplete for 3 systems
3. Section 14: Two metrics without current values

Recommendations:
1. Add win rate data against top 3 competitors
2. Verify and add versions for CRM, ERP, HR systems
3. Fill current values for employee satisfaction, CAC metrics
```

---

## Troubleshooting

### Commands Not Showing

If `/BizContext/` doesn't autocomplete:
1. Make sure you're in the repository root directory
2. Check that `.claude/commands/BizContext/` folder exists
3. Restart Claude Code

### Agent Not Challenging Content

If the agent accepts everything:
- This shouldn't happen by design
- Try `/BizContext/critique` on specific content
- Report as issue if persistent

### Session Lost

Progress is saved to `my-business-context.yaml`. To resume:
```
/BizContext/start
```
The agent will detect existing progress.

---

## Related Documentation

- [Usage Guide](usage-guide.md) - Manual template filling guide
- [Best Practices](best-practices.md) - Writing effective business context
- [Anti-Patterns](../.bizcontext-core/data/anti-patterns.md) - Common mistakes to avoid
- [Good Examples](../.bizcontext-core/data/good-examples.md) - Examples of quality content

---

## Support

- **Issues**: [GitHub Issues](https://github.com/Latentti/business-context-ai-template/issues)
- **Questions**: [GitHub Discussions](https://github.com/Latentti/business-context-ai-template/discussions)

---

**Ready to start?**

```bash
cd business-context-ai-template
claude
/BizContext/start
```
