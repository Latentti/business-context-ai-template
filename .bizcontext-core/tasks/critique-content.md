# Critique Content Task

## Purpose
Evaluate content from an AI-usefulness perspective. Determine if the content helps AI make better development decisions.

## Core Question
For every piece of content, ask: **"How would an AI developer use this information?"**

## Evaluation Framework

### Dimension 1: AI-Usefulness (1-5)

| Score | Description | Example |
|-------|-------------|---------|
| 5 | Directly guides technical decisions | "PostgreSQL 15 on AWS RDS, 10TB, needs to handle 50K writes/sec" |
| 4 | Provides clear constraints | "GDPR requires EU data residency, 72h breach notification" |
| 3 | Useful context | "Customers are primarily Finnish SMBs in retail" |
| 2 | Vague but somewhat helpful | "We have enterprise customers" |
| 1 | Marketing fluff | "We deliver innovative solutions" |

**Questions to determine score:**
- Can AI make a specific technical recommendation based on this?
- Does this constrain or guide solution design?
- Would removing this change AI's output?

### Dimension 2: Specificity (1-5)

| Score | Description | Example |
|-------|-------------|---------|
| 5 | Exact numbers with context | "127 customers, €8.2M ARR, 67 employees" |
| 4 | Ranges with meaning | "50-100 concurrent users during peak (9-11 AM Finnish time)" |
| 3 | Approximate with qualification | "Around €5M revenue (audited financials pending)" |
| 2 | Vague quantities | "Many customers in financial services" |
| 1 | No quantification | "We serve major enterprises" |

### Dimension 3: Factual Accuracy (1-5)

| Score | Description | Indicators |
|-------|-------------|------------|
| 5 | Verifiable facts with sources | Metrics, dates, named sources |
| 4 | Factual but unverified | Reasonable claims, likely accurate |
| 3 | Mix of fact and opinion | Some facts, some unsupported claims |
| 2 | Mostly opinion | "We believe", "We think", claims without evidence |
| 1 | Marketing statements | Superlatives, buzzwords, unverifiable claims |

## Critique Process

### Step 1: Read and Categorize
```
Analyzing: "{content}"

Initial Assessment:
- Type: {fact/claim/opinion/marketing}
- Relevance: {direct/contextual/minimal}
- Completeness: {complete/partial/missing_key_info}
```

### Step 2: Score Each Dimension
```
## CRITIQUE SCORES

| Dimension | Score | Reason |
|-----------|-------|--------|
| AI-Usefulness | {1-5} | {reason} |
| Specificity | {1-5} | {reason} |
| Factual Accuracy | {1-5} | {reason} |

**Overall Score: {average}/5**
```

### Step 3: Provide Actionable Feedback
```
## IMPROVEMENT RECOMMENDATIONS

### Current State
"{current_content}"

### Issues
1. {Issue 1}
2. {Issue 2}

### Improved Version
"{suggested_improvement}"

### Why This Is Better
- AI-Usefulness: {how this helps AI}
- Specificity: {what specifics were added}
- Factual: {how this is more verifiable}
```

### Step 4: Offer Options
```
Options:
1. Accept improved version
2. Provide your own revision
3. Explain why current version should stay
4. Get more examples

Select 1-4:
```

## Common Critique Patterns

### Pattern: Generic Value Proposition
```
❌ "We help businesses grow with innovative solutions"

Critique:
- AI-Usefulness: 1/5 - Zero technical guidance
- Specificity: 1/5 - No specifics at all
- Factual: 1/5 - Pure marketing

✅ "B2B SaaS platform for inventory management. Reduces overstock by
avg 23% (based on 45 customer case studies). Integrates with SAP,
Oracle ERP, and 15 popular POS systems via REST API."

Why better: AI now knows the domain, typical outcomes, and integration requirements.
```

### Pattern: Vague Technical Description
```
❌ "Modern cloud-based architecture using latest technologies"

Critique:
- AI-Usefulness: 2/5 - "Cloud" is somewhat useful, but nothing actionable
- Specificity: 1/5 - No specifics
- Factual: 2/5 - Probably true but unverifiable

✅ "AWS-hosted (eu-north-1), Kubernetes 1.29 on EKS. Microservices in
TypeScript/Node.js 20, data in PostgreSQL 15 (RDS) and Redis 7.
Monthly AWS spend: €35-40K. Technical debt: Legacy reporting service
(Python 3.8) needs rewrite."

Why better: AI knows exact stack, versions, scale (via cost), and constraints.
```

### Pattern: Aspirational as Current
```
❌ "We have a data-driven culture with advanced analytics capabilities"

Critique:
- AI-Usefulness: 2/5 - Suggests analytics focus but unclear what exists
- Specificity: 1/5 - What does "advanced" mean?
- Factual: 2/5 - "Data-driven culture" is opinion

✅ "Analytics stack: Metabase for dashboards (15 active users), dbt for
transformations, BigQuery for warehouse (2TB, growing 100GB/month).
Maturity: Can do descriptive analytics well, predictive is aspirational
(no data science team yet)."

Why better: Honest about current state vs aspiration.
```

## Critique Report Template

```markdown
# CONTENT CRITIQUE

**Content:** "{content_snippet}"
**Section:** {section_name}
**Field:** {field_name}

---

## Scores

| Dimension | Score | Assessment |
|-----------|-------|------------|
| AI-Usefulness | {X}/5 | {brief_reason} |
| Specificity | {X}/5 | {brief_reason} |
| Factual Accuracy | {X}/5 | {brief_reason} |
| **Overall** | **{avg}/5** | **{verdict}** |

---

## Analysis

**What AI Can Use:**
{list_of_usable_elements}

**What AI Cannot Use:**
{list_of_unusable_elements}

**Missing Information:**
{list_of_gaps}

---

## Recommendations

**Priority 1:** {most_important_fix}
**Priority 2:** {second_fix}
**Priority 3:** {third_fix}

---

## Improved Version

```yaml
{improved_yaml_content}
```

---

## Next Action

{What user should do next}
```
