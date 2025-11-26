# Business Context Quality Checklist

Use this checklist to validate your business context document before using it for AI development.

## Overall Document Quality

### Completeness
- [ ] All required sections have content
- [ ] No placeholder text remaining (`[Your company]`, `TBD`, `TODO`, etc.)
- [ ] No empty arrays or objects where content is expected
- [ ] Document has been reviewed by someone who knows the business

### Consistency
- [ ] Employee counts are consistent across all sections
- [ ] Revenue figures match across mentions
- [ ] Technology references are consistent (same names, versions)
- [ ] Timeline references don't contradict each other
- [ ] Market position claims are consistent

### Currency
- [ ] Document has been updated within last 6 months
- [ ] Metrics reflect current state (not outdated data)
- [ ] Technology versions are current
- [ ] Strategic objectives reflect current plans

---

## Section-Specific Checks

### 1. Executive Summary
- [ ] Has specific revenue number (not range like "multi-million")
- [ ] Has exact employee count
- [ ] Has exact customer count
- [ ] Market position claim has supporting data
- [ ] Competitive advantage is specific and evidenced
- [ ] Vision has timeframe and measurable goal

### 2. Company Profile
- [ ] Organizational structure is current
- [ ] Department sizes add up to total employees
- [ ] Leadership team is complete and current
- [ ] Culture description is factual, not aspirational

### 3. Business History
- [ ] Key milestones have specific dates
- [ ] Business model evolution is explained
- [ ] Strategic pivots are documented with reasons

### 4. Core Business & Value Proposition
- [ ] Value proposition is specific, not generic
- [ ] Revenue streams have percentages
- [ ] Business model is clearly explained
- [ ] Customer benefits are quantified where possible

### 5. Products and Services
- [ ] All products/services are listed
- [ ] Each has technical details (not just marketing description)
- [ ] Metrics per product (users, revenue contribution)
- [ ] Lifecycle stage is indicated
- [ ] Pricing model is clear

### 6. Customer Segments
- [ ] Segments are defined with specific criteria
- [ ] Segment sizes are quantified
- [ ] Needs are specific, not generic
- [ ] Buying behavior is documented
- [ ] Segment metrics included (CLTV, CAC, churn)

### 7. Competitive Landscape
- [ ] Competitors are named (not "Competitor A")
- [ ] Win/loss analysis is honest
- [ ] Our weaknesses are acknowledged
- [ ] Differentiation claims have evidence

### 8. Business Capabilities
- [ ] Maturity assessments are honest (not all 4s and 5s)
- [ ] Gaps are clearly identified
- [ ] No inflated self-assessment
- [ ] Technology enablement is specified

### 9. Business Processes
- [ ] Key processes are documented
- [ ] Pain points are identified
- [ ] Metrics are included (cycle time, error rate)
- [ ] Improvement opportunities noted

### 10. Technology Landscape ⭐ CRITICAL
- [ ] ALL major systems are listed
- [ ] Versions are included
- [ ] Technical debt is honestly assessed
- [ ] Integrations are documented
- [ ] Cloud details are specific (region, services, spend)
- [ ] Architecture style is accurately described
- [ ] No contradictions (e.g., "microservices" but main app is monolith)

### 11. Data and Analytics
- [ ] Data assets are inventoried
- [ ] Data volumes are quantified
- [ ] Data quality is honestly assessed
- [ ] Governance is described
- [ ] AI/ML capabilities are accurately stated (not aspirational)

### 12. Operating Model
- [ ] Decision rights are clear
- [ ] Governance bodies are listed
- [ ] Work methodology is specified
- [ ] Actual practices, not aspirational

### 13. Strategic Objectives
- [ ] Objectives are measurable
- [ ] Timelines are specified
- [ ] Initiatives have owners
- [ ] No vague aspirations without metrics

### 14. Success Metrics
- [ ] All metrics have current values
- [ ] Targets are defined
- [ ] North star metric is identified
- [ ] Trends are indicated

### 15. Constraints and Requirements ⭐ CRITICAL
- [ ] Regulations are listed with specific requirements
- [ ] Security requirements are specific (not just "must be secure")
- [ ] Performance requirements are measurable
- [ ] Budget constraints are stated
- [ ] Compliance implications are clear
- [ ] Technology constraints are documented

### 16. Stakeholders
- [ ] Key decision makers identified
- [ ] Decision authority is clear
- [ ] Communication preferences noted
- [ ] Change readiness assessed

### 17. Partnerships and Ecosystem
- [ ] Key partners are named
- [ ] Dependencies are clear
- [ ] Contract status noted where relevant

### 18. Risks and Challenges
- [ ] Risks are specific, not generic
- [ ] Likelihood and impact assessed
- [ ] Mitigations described
- [ ] Current challenges documented

### 19. Organizational Culture
- [ ] Culture described factually, not marketed
- [ ] Change capacity assessed honestly
- [ ] Communication style documented

### 20. AI Development Context
- [ ] Current AI usage documented accurately
- [ ] Preferences are stated
- [ ] Review requirements are clear
- [ ] Success criteria defined

### 21. Lessons Learned
- [ ] Specific examples given
- [ ] Anti-patterns documented
- [ ] Preferences are reasoned

### 22. Future Vision
- [ ] Vision has timeframe
- [ ] Goals are measurable
- [ ] Not just marketing language

---

## Red Flag Checklist

If ANY of these are present, the document needs revision:

### Marketing Language
- [ ] No "leading" without market share data
- [ ] No "innovative" without specific innovation
- [ ] No "world-class" without benchmark
- [ ] No "best-in-class" without comparison
- [ ] No "cutting-edge" without specifics

### Vague Quantities
- [ ] No "many" - use exact numbers
- [ ] No "several" - use exact numbers
- [ ] No "significant" - use percentages
- [ ] No "various" - list them
- [ ] No "numerous" - count them

### Missing Evidence
- [ ] No claims without supporting data
- [ ] No superlatives without proof
- [ ] No market position without share data
- [ ] No performance claims without metrics

### Inconsistencies
- [ ] Numbers add up correctly
- [ ] No conflicting information
- [ ] Technology mentions are consistent
- [ ] Timeline references align

---

## Scoring Guide

Calculate your document quality score:

**Completeness (25 points)**
- All 22 sections filled: 25 points
- 18-21 sections: 20 points
- 14-17 sections: 15 points
- 10-13 sections: 10 points
- <10 sections: 5 points

**Specificity (25 points)**
- All metrics have numbers: 25 points
- Most metrics have numbers: 20 points
- Some metrics have numbers: 15 points
- Few metrics have numbers: 10 points
- Mostly vague: 5 points

**Accuracy (25 points)**
- No marketing language: 25 points
- 1-2 instances: 20 points
- 3-5 instances: 15 points
- 6-10 instances: 10 points
- Pervasive: 5 points

**Consistency (25 points)**
- No inconsistencies: 25 points
- 1 inconsistency: 20 points
- 2-3 inconsistencies: 15 points
- 4-5 inconsistencies: 10 points
- Many: 5 points

**Total Score Interpretation:**
- 90-100: Excellent - Ready for AI use
- 75-89: Good - Minor improvements recommended
- 60-74: Adequate - Several improvements needed
- 40-59: Needs Work - Significant revision required
- <40: Not Ready - Major rewrite needed

---

## Final Validation

Before declaring the document complete:

1. [ ] Run the `/BizContext/validate` command
2. [ ] Score is 80 or above
3. [ ] No critical issues remaining
4. [ ] Document reviewed by business stakeholder
5. [ ] Document reviewed by technical stakeholder
6. [ ] Update schedule established (quarterly recommended)
