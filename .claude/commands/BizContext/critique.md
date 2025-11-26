# /BizContext/critique - Critically Evaluate Content

When this command is used, execute the following fact-checking and critique workflow:

## PURPOSE

Evaluate provided content (section, field, or entire document) for:
1. AI-usefulness
2. Specificity
3. Factual accuracy
4. Marketing language
5. Missing information

## CRITIQUE WORKFLOW

### Step 1: Identify Target

If no target specified, ask:
```
What would you like me to critique?

1. A specific section (provide section name)
2. A piece of text you'll paste
3. The entire document
4. Current working content

Select or paste content:
```

### Step 2: Apply Critique Framework

For each piece of content, evaluate against these criteria:

#### A. AI-Usefulness Check
```
🤖 AI-USEFULNESS SCORE: {1-5}/5

Questions:
- Can AI make a development decision based on this? {yes/no}
- Does this constrain or guide technical choices? {yes/no}
- Would removing this change AI's recommendations? {yes/no}

Verdict: {USEFUL / NEEDS IMPROVEMENT / NOT USEFUL}
```

#### B. Specificity Check
```
🎯 SPECIFICITY SCORE: {1-5}/5

Red Flags Found:
{list any vague terms found}

Missing Specifics:
{list what numbers/details are missing}

Verdict: {SPECIFIC / NEEDS DETAIL / TOO VAGUE}
```

#### C. Fact vs Marketing Check
```
📊 FACTUAL SCORE: {1-5}/5

Marketing Language Found:
{list any marketing terms}

Unverified Claims:
{list claims without evidence}

Verdict: {FACTUAL / NEEDS EVIDENCE / MARKETING FLUFF}
```

### Step 3: Provide Improvement Recommendations

```
## CRITIQUE SUMMARY

**Overall Quality Score: {average}/5**

### Issues Found:

1. **{issue_type}**: {description}
   - Current: "{problematic_text}"
   - Suggested: "{improved_text}"

2. **{issue_type}**: {description}
   - Current: "{problematic_text}"
   - Suggested: "{improved_text}"

### Missing Information:
- {list of missing but important details}

### Strengths:
- {list what's working well}

---

Would you like me to:
1. Help fix the issues one by one
2. Show examples of excellent content for this section
3. Explain why these changes matter for AI
4. Apply all suggested fixes automatically

Select 1-4:
```

## COMMON CRITIQUE PATTERNS

### Pattern: Superlatives Without Data
```
FOUND: "We are the leading provider..."

CRITIQUE:
- "Leading" by what measure?
- Market share percentage?
- Customer count vs competitors?
- Award or recognition?

IMPROVED: "Largest provider in Finland with 34% market share (2024 Gartner report), serving 127 of the top 200 Finnish companies"
```

### Pattern: Vague Technology Claims
```
FOUND: "Modern cloud-based architecture"

CRITIQUE:
- Which cloud provider(s)?
- What architecture pattern?
- When was it modernized?
- What's still legacy?

IMPROVED: "AWS-hosted microservices (EKS), migrated from monolith in 2022. 85% of services containerized, 15% legacy Java monolith scheduled for decomposition Q2 2025"
```

### Pattern: Missing Constraints
```
FOUND: "We need the system to be fast and reliable"

CRITIQUE:
- What response time is acceptable?
- What uptime is required?
- What's the SLA commitment?
- What happens if these aren't met?

IMPROVED: "P99 latency <200ms, 99.9% uptime SLA. Penalty: 10% service credit per 0.1% below target. Current performance: P99 145ms, 99.94% uptime (2024 YTD)"
```

### Pattern: Opinion as Fact
```
FOUND: "Our team is highly skilled"

CRITIQUE:
- By what measure?
- Certifications?
- Experience levels?
- Retention rates?

IMPROVED: "Engineering team: 45 developers, avg 8 years experience. 12 AWS certified, 8 with CS degrees from top-10 Finnish universities. 94% retention rate (2024)"
```

## AUTOMATIC PATTERNS TO FLAG

Always immediately flag these patterns:

| Pattern | Example | Action |
|---------|---------|--------|
| Superlatives | "best", "leading", "top" | Demand metric |
| Vague quantities | "many", "several", "few" | Demand number |
| Marketing adjectives | "innovative", "cutting-edge" | Demand evidence |
| Passive claims | "is considered", "is known for" | Demand source |
| Future promises | "will be", "planning to" | Clarify timeline |
| Hedging | "approximately", "around" | Get exact or range |
