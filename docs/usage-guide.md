# Usage Guide - Business Context AI Template

Complete step-by-step guide to creating your business context for AI development tools.

---

## Table of Contents

1. [Getting Started](#getting-started)
2. [Choosing the Right Template](#choosing-the-right-template)
3. [Filling Out the Template](#filling-out-the-template)
4. [Section-by-Section Guide](#section-by-section-guide)
5. [Quality Checklist](#quality-checklist)
6. [Using Your Context](#using-your-context)
7. [Next Steps](#next-steps)

---

## Getting Started

### Prerequisites

Before you begin, gather these materials:

- ✅ Company strategy documents
- ✅ Product/service descriptions
- ✅ Technology architecture documentation
- ✅ Organizational charts
- ✅ Customer/market research
- ✅ Financial metrics (if available/relevant)
- ✅ Compliance and regulatory requirements

### Time Investment

- **Quick Start**: 4-6 hours
- **Full Template**: 8-16 hours
- **Enterprise Template**: 16-40 hours

**Recommendation**: Spread the work over multiple sessions rather than one marathon session. Your context will be better quality.

### Who Should Be Involved?

**Ideal approach**: Cross-functional team

- **Business Leader** (CEO, VP): Strategy, vision, business model
- **Product Manager**: Products, customers, market positioning
- **CTO/Tech Lead**: Technology landscape, architecture, constraints
- **Operations Manager**: Processes, workflows, operational context
- **Enterprise Architect** (if available): TOGAF expertise, capability modeling

**Minimum viable**: One person with broad business knowledge can fill most sections, then validate with stakeholders.

---

## Choosing the Right Template

### Quick Start Template (10 sections, 4-6 hours)

**Use when:**
- You want to get started quickly
- You're a startup or small company
- You have simple organizational structure
- You need immediate value and can expand later

**Covers:**
- Executive Summary
- Products and Services
- Customer Segments
- Technology Stack
- Constraints and Requirements
- Strategic Objectives
- Success Metrics
- Organizational Context
- AI Development Preferences
- Quick Reference Links

**Best for:**
- Startups
- Small teams (< 50 people)
- Single-product companies
- Simple tech stacks
- Fast iteration needed

---

### Full Template (22 sections, 8-16 hours)

**Use when:**
- You want comprehensive coverage
- You have multiple products or business units
- Your organization is moderately complex
- You want TOGAF-compliant business architecture
- You run multiple concurrent AI projects

**Covers:**
- All Quick Start sections PLUS:
- Business History and Evolution
- Detailed Business Capabilities (TOGAF model)
- Business Processes and Value Streams
- Data and Analytics Strategy
- Operating Model
- Partnerships and Ecosystem
- Risk Management
- Organizational Culture
- Lessons Learned
- Future Vision
- And more...

**Best for:**
- Scale-ups
- Mid-size companies (50-500 people)
- Multiple products/services
- Moderate organizational complexity
- Regular AI-driven development

---

### Enterprise Template (Extended, 16-40 hours)

**Use when:**
- You're a large organization (500+ people)
- You have multiple business units
- Complex product portfolios
- Heavy regulatory requirements
- Need rigorous governance
- Enterprise architecture mandate

**Includes:**
- Everything from Full Template PLUS:
- Multi-BU capability models
- Detailed governance frameworks
- Compliance matrices
- Stakeholder matrices
- Integration architecture
- And more enterprise-specific sections

**Best for:**
- Large enterprises
- Heavily regulated industries
- Complex organizational structures
- Formal EA practices

---

## Filling Out the Template

### General Principles

#### 1. **Be Specific, Not Generic**

❌ **Bad**: "We have great technology and good customer service"

✅ **Good**: "We run AI-powered demand forecasting in production serving 500K+ customers with 99.97% uptime. Our ML models process 20M transactions/year."

#### 2. **Quantify Everything Possible**

❌ **Bad**: "Many customers", "Fast-growing", "Good performance"

✅ **Good**: "500,000 customers", "40% YoY growth", "< 200ms P95 response time"

#### 3. **Explain the 'Why' Behind Decisions**

❌ **Bad**: "We use PostgreSQL"

✅ **Good**: "We standardized on PostgreSQL after 2021 incident where MySQL replication lag caused financial discrepancies. PostgreSQL's synchronous replication and ACID compliance are critical for our financial systems."

#### 4. **Include Constraints and Anti-Patterns**

Don't just describe what you do - describe what you DON'T do and why.

✅ **Good**:
```yaml
prohibited_technologies:
  - technology: "MongoDB for financial transactions"
    reason: "Experienced data consistency issues in 2020.
    All financial data must use ACID-compliant SQL databases."
```

#### 5. **Write for AI, Not Marketing**

AI needs facts, specifics, and context - not buzzwords and hype.

❌ **Marketing speak**: "Revolutionary game-changing innovation disrupting the industry"

✅ **AI context**: "#3 market share in Finnish parking management (15%), differentiated by production-scale AI (vs competitors piloting), serving 500K users"

---

### Starting Point Recommendations

#### Option A: Top-Down (Recommended for most)

1. Start with **Executive Summary** (30 min)
   - Forces you to clarify the essentials
   - Easier to expand sections later

2. Fill **Products and Services** (1-2 hours)
   - What you actually do/sell
   - Core business understanding

3. Add **Technology Landscape** (1-2 hours)
   - Critical for AI to make technical decisions
   - Tech stack, architecture, constraints

4. Complete **Constraints and Requirements** (1-2 hours)
   - Regulatory, security, performance requirements
   - AI must respect these boundaries

5. Expand remaining sections as time permits

#### Option B: Bottom-Up (For technical teams)

1. Start with **Technology Landscape**
2. Add **Constraints and Requirements**
3. Fill **Products and Services**
4. Work backwards to strategy and business model
5. Finish with **Executive Summary**

#### Option C: Inside-Out (For product-focused teams)

1. Start with **Products and Services**
2. Add **Customer Segments**
3. Fill **Value Proposition**
4. Expand to technology and operations
5. Add strategy and governance

**No wrong approach** - choose what feels natural for your team.

---

## Section-by-Section Guide

### Priority 1: MUST HAVE (Foundation)

These sections are critical for AI to understand your business:

#### 1. Executive Summary

**Time**: 30-60 minutes

**Key Elements**:
- One-sentence company description
- Key metrics (revenue, customers, employees)
- Core differentiator (what makes you unique)
- 3-5 year vision

**Tips**:
- Think "elevator pitch" but with specifics
- Include quantitative metrics
- Be honest about current state

**Common Mistakes**:
- Too vague ("We're innovative")
- Too long (keep it concise)
- Missing key metrics

---

#### 4. Core Business & Value Proposition

**Time**: 1-2 hours

**Key Elements**:
- What you do and for whom
- Why customers choose you vs. competitors
- Business model canvas (how you create/capture value)
- Revenue streams

**Tips**:
- Focus on customer pain points you solve
- Be specific about differentiation
- Explain the economics (how you make money)

**Common Mistakes**:
- Generic value props ("quality, service, innovation")
- Not explaining WHY you're different
- Missing the business model

---

#### 5. Products and Services

**Time**: 2-4 hours

**Key Elements**:
- Detailed product/service descriptions
- Target customers for each
- Key features and capabilities
- Competitive positioning
- Business metrics (users, revenue, strategic importance)

**Tips**:
- One product/service at a time
- Include technical details (AI will need them)
- Explain strategic importance
- Note interdependencies

**Common Mistakes**:
- Too high-level ("We have a platform")
- Missing technical architecture
- Not explaining customer segments per product

---

#### 10. Technology Landscape

**Time**: 2-4 hours

**Key Elements**:
- Application portfolio (all major systems)
- Technical architecture (microservices, monolithic, etc.)
- Infrastructure (cloud providers, hosting model)
- Integration patterns
- Technology standards and principles

**Tips**:
- Be brutally honest about technical debt
- Include versions where relevant
- Note what's legacy vs. modern
- Explain technology choices (the "why")

**Common Mistakes**:
- Too vague ("We use modern technologies")
- Hiding technical debt
- Missing integration complexity
- Not explaining constraints

---

#### 15. Constraints and Requirements

**Time**: 2-4 hours

**Key Elements**:
- Regulatory compliance (GDPR, HIPAA, PCI-DSS, etc.)
- Security requirements
- Performance requirements (SLAs)
- Technology constraints
- Budget and timeline constraints

**Tips**:
- Be specific about compliance requirements
- Include implications ("This means...")
- Note what AI CANNOT do
- Explain budget/timeline realities

**Common Mistakes**:
- Missing regulatory requirements
- Vague security requirements
- Not explaining implications
- Forgetting organizational constraints

---

### Priority 2: HIGHLY RECOMMENDED (Context)

#### 6. Customer Segments

**Time**: 1-3 hours

**Key Elements**:
- Detailed customer profiles
- Pain points and desired outcomes
- How you solve their problems
- Buying behavior
- Segment metrics

**Tips**:
- One segment at a time
- Be specific about characteristics
- Include quantitative data
- Note market strength per segment

---

#### 8. Business Capabilities (TOGAF)

**Time**: 2-4 hours

**Key Elements**:
- Capability model (what your business can do)
- Current vs. target maturity
- Strategic importance
- Gaps and investment priorities

**Tips**:
- Use TOGAF capability domains as starting point
- Rate maturity honestly (1-5 scale)
- Focus on capabilities needing development
- Connect to strategic objectives

**Note**: This is one of the more complex sections. See [TOGAF capability modeling](https://www.businessarchitectureguild.org/page/Capabilities) for guidance.

---

#### 13. Strategic Objectives

**Time**: 1-2 hours

**Key Elements**:
- Major strategic goals
- Timelines and success metrics
- Key initiatives supporting objectives
- Transformation programs

**Tips**:
- Connect objectives to measurable outcomes
- Explain WHY each objective matters
- Note dependencies and risks
- Be realistic about timelines

---

#### 14. Success Metrics

**Time**: 1-2 hours

**Key Elements**:
- Financial metrics
- Customer metrics
- Operational metrics
- Product metrics
- North Star metric (the ONE most important)

**Tips**:
- Include current and target values
- Explain what drives each metric
- Note which metrics are most critical
- Show how metrics connect to objectives

---

### Priority 3: GOOD TO HAVE (Depth)

Fill these as time permits - they add valuable context but aren't critical for basic AI operation:

- **2. Company Profile**: Org structure, leadership, culture
- **3. Business History**: How you got here, evolution
- **7. Competitive Landscape**: Market positioning, competitors
- **9. Business Processes**: How work flows through your organization
- **11. Data and Analytics**: Data assets and capabilities
- **12. Operating Model**: How your organization works
- **16. Stakeholders**: Key decision makers
- **17. Partnerships**: Ecosystem and key partners
- **18. Risks**: Business risks and challenges
- **19. Culture**: Organizational dynamics
- **20. AI Development Context**: How you work with AI tools
- **21. Lessons Learned**: Past mistakes and preferences
- **22. Future Vision**: Long-term aspirations

---

## Quality Checklist

Before finalizing your business context, review against this checklist:

### Completeness

- [ ] All Priority 1 (MUST HAVE) sections complete
- [ ] All Priority 2 (HIGHLY RECOMMENDED) sections complete (or consciously skipped)
- [ ] No placeholder text ([FILL IN]) remaining
- [ ] All relevant sections for your business included

### Specificity

- [ ] Numbers and metrics instead of vague terms
- [ ] Specific technology names and versions
- [ ] Clear regulatory requirements with details
- [ ] Concrete examples, not abstract descriptions

### Accuracy

- [ ] Validated by relevant stakeholders
- [ ] Technical details reviewed by engineering
- [ ] Business details reviewed by business leaders
- [ ] Compliance requirements verified
- [ ] No contradictions between sections

### AI-Readiness

- [ ] Explains "why" behind decisions, not just "what"
- [ ] Includes constraints and anti-patterns
- [ ] Provides sufficient technical detail
- [ ] Captures organizational context
- [ ] Written for machine consumption (clear, structured)

### Maintenance

- [ ] Version number set
- [ ] Last updated date current
- [ ] Document owner identified
- [ ] Review frequency defined
- [ ] In version control (Git)

---

## Using Your Context

### In AI Development Tools

#### Claude Code / Claude Projects

```
# At start of project:
"Before we begin, please read and internalize the business context at:
[path-to-your-context.yaml]

This provides complete context about:
- Our business and products
- Technology stack and constraints
- Strategic objectives
- How we work

Now for THIS specific project: [project details]"
```

#### GitHub Copilot Workspaces

```markdown
# In .github/copilot-instructions.md:

# Business Context

See `docs/business-context.yaml` for complete business context including:
- Technology standards: Section 10
- Security requirements: Section 15
- Coding preferences: Section 20
```

#### Custom AI Tools

```python
# Load context into your AI tool
with open('business-context.yaml', 'r') as f:
    business_context = yaml.safe_load(f)

# Include in system prompt
system_prompt = f"""
You are a developer working for {business_context['company_name']}.

Key Context:
- Products: {business_context['products_and_services']}
- Tech Stack: {business_context['technology_landscape']}
- Constraints: {business_context['constraints_and_requirements']}

Respect all constraints and requirements when generating code.
"""
```

### In Other Scenarios

**New Developer Onboarding**:
"Read `docs/business-context.yaml` for comprehensive company overview"

**Vendor/Consultant Briefing**:
"See attached business context for complete understanding of our organization"

**RFP Responses**:
Reference sections to ensure vendors understand your environment

**Strategic Planning**:
Use as baseline for strategy discussions and planning

---

## Next Steps

After creating your business context:

### 1. Validate (1-2 hours)

- Review with key stakeholders
- Technical review by engineering lead
- Business review by product/business leader
- Compliance review if in regulated industry

### 2. Version Control (15 minutes)

```bash
git add business-context.yaml
git commit -m "Initial business context v1.0"
git tag v1.0
```

### 3. Publish Internally (30 minutes)

- Add to documentation site
- Announce to team
- Add to onboarding materials
- Link from developer guides

### 4. Use in Next Project (Immediate)

Test drive your context in the next AI-driven project:
- Note what questions AI still asks
- Identify gaps in your context
- Refine and iterate

### 5. Schedule Maintenance (15 minutes)

- Add quarterly review to calendar
- Identify document owner
- Set up change notification process
- Create update workflow

---

## Common Questions

### "How long does this really take?"

**Realistic times:**
- **Quick Start**: 4-6 hours (spread over 2-3 sessions)
- **Full Template**: 8-16 hours (spread over 3-5 sessions)
- **Enterprise**: 16-40 hours (spread over 5-10 sessions)

**Pro tip**: Don't try to do it all at once. Better quality if done in sessions.

### "Can I use this if my business is constantly changing?"

**Yes!** Focus on:
- What stays stable (values, general approach, core products)
- Strategic direction (where you're heading, even if details change)
- Update frequently (quarterly for fast-changing businesses)

### "What if I don't know some information?"

**Options:**
1. **Mark as "N/A"** with reason
2. **Use placeholder** and note "TO BE DETERMINED"
3. **Fill what you know**, skip what you don't
4. **Research and fill** (opportunity to clarify unknowns)

Start with what you know, iterate to fill gaps.

### "Should this be confidential?"

**Usually yes.** This contains:
- Strategic information
- Technology details
- Financial metrics
- Competitive positioning

**Recommendation**: Treat as "Internal - Confidential". Can create sanitized public version if needed.

### "What format should I use?"

**YAML is recommended** because:
- Structured (easy for AI to parse)
- Readable (humans can read/edit)
- Flexible (easy to extend)
- Standard (widely supported)

**Alternatives:**
- **Markdown**: Better readability, less structured
- **JSON**: More structured, less readable
- **Notion/Confluence**: Collaborative editing, but export to YAML for AI use

### "Can I customize the template?"

**Absolutely!** The template is a starting point:

**Add sections** for:
- Industry-specific requirements
- Regional considerations
- Unique business model elements

**Remove sections** that:
- Don't apply to your business
- Are truly N/A (not just unknown)

**Reorganize** if:
- Different flow makes more sense
- Your organization prefers different structure

---

## Additional Resources

- **[Best Practices Guide](best-practices.md)** - Writing effective context
- **[Maintenance Guide](maintenance-guide.md)** - Keeping context current
- **[FAQ](faq.md)** - More questions and answers
- **[Examples](../examples/)** - See filled examples

---

**Ready to start?** Choose your template and begin filling it out!

[← Back to Main README](../README.md) | [Best Practices →](best-practices.md)
