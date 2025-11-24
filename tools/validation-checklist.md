# Business Context Validation Checklist

Ensure your business context is complete, accurate, and AI-ready before using it in projects.

---

## 🎯 Purpose

This checklist helps you validate that your business context:
- Is complete enough for AI to make good decisions
- Contains accurate, up-to-date information
- Is specific enough to be useful
- Follows best practices

---

## ✅ Completeness Check

### Critical Sections (Must be complete)

- [ ] **Section 1: Executive Summary**
  - Company name, tagline, metrics present
  - Competitive advantage is specific
  - Vision is clear

- [ ] **Section 4: Core Business & Value Proposition**
  - Value proposition explains WHY, not just WHAT
  - Customer benefits are specific
  - Business model documented

- [ ] **Section 5: Products and Services**
  - All major products documented
  - Target customers identified
  - Business metrics included

- [ ] **Section 10: Technology Landscape**
  - Tech stack with versions
  - Architecture style documented
  - Technical constraints explained

- [ ] **Section 15: Constraints and Requirements**
  - Regulatory requirements specific
  - Security requirements detailed
  - Performance SLAs stated

### Recommended Sections (Should be complete)

- [ ] Section 6: Customer Segments
- [ ] Section 7: Competitive Landscape
- [ ] Section 8: Business Capabilities
- [ ] Section 13: Strategic Objectives
- [ ] Section 14: Success Metrics

---

## 🔍 Quality Check

### Specificity Test

For each major section, verify:

- [ ] **No Vague Language**
  - ❌ "We're innovative" → ✅ "We use AI in production (20M transactions/year)"
  - ❌ "Many customers" → ✅ "500,000 active customers"
  - ❌ "Fast performance" → ✅ "< 200ms P95 response time"

- [ ] **Numbers, Not Adjectives**
  - All metrics have actual numbers
  - Growth rates are percentages
  - Timelines are specific dates or durations

- [ ] **Examples, Not Just Descriptions**
  - Customer segments have example companies
  - Use cases include concrete scenarios
  - Technology choices explain why

### Explanation Test

- [ ] **Every Constraint Has a "Why"**
  - "We use PostgreSQL" → "We use PostgreSQL because [incident that taught us]"
  - "GDPR required" → "GDPR required: affects [specific features] by [implications]"
  - "Must scale to X" → "Must scale to X because [business driver]"

- [ ] **Every Technology Choice Justified**
  - Framework selections explained
  - Architecture decisions documented
  - Trade-offs acknowledged

### Accuracy Test

- [ ] **Metrics Are Current**
  - Revenue numbers are from last year or current year
  - Customer counts are up-to-date
  - Employee count is accurate
  - Growth rates are recent

- [ ] **Technology Is Current**
  - Framework versions are correct
  - Legacy systems acknowledged
  - Migration status accurate

- [ ] **Strategy Is Current**
  - Strategic objectives reflect current direction
  - Vision aligns with recent leadership communications
  - No outdated initiatives

---

## 📝 Content Quality

### Writing Quality

- [ ] **No Placeholder Text**
  - No [FILL IN] or [TBD] markers
  - No "Lorem ipsum" or dummy text
  - All sections have real content

- [ ] **No Marketing Buzzwords**
  - ❌ "Revolutionary", "game-changing", "disruptive"
  - ❌ "Best-in-class", "world-class", "cutting-edge"
  - ✅ Specific capabilities and provable claims

- [ ] **Consistent Terminology**
  - Product names consistent throughout
  - Company name used consistently
  - Technical terms used consistently

### Structure Quality

- [ ] **YAML Syntax Valid**
  ```bash
  # Test with:
  python -c "import yaml; yaml.safe_load(open('your-context.yaml'))"
  ```

- [ ] **Indentation Correct**
  - Consistent 2-space indentation
  - Nested structures properly aligned

- [ ] **No Broken References**
  - All "see Section X" references are correct
  - All internal links work

---

## 🔐 Security & Privacy Check

### Confidential Information

- [ ] **No Sensitive Data Exposed**
  - No actual customer names (unless public/approved)
  - No specific revenue numbers (if confidential)
  - No proprietary algorithms or trade secrets
  - No security implementation details
  - No internal system passwords or keys

- [ ] **Appropriate Level of Detail**
  - Enough for AI to work effectively
  - Not so much that competitors benefit
  - Security by obscurity avoided

### Compliance

- [ ] **Regulatory Requirements Documented**
  - GDPR compliance requirements stated
  - Industry-specific regulations noted
  - Compliance implications for AI explained

---

## 🎭 Stakeholder Validation

### Technical Review

- [ ] **Reviewed by Engineering Lead**
  - Technology landscape accurate
  - Technical constraints correct
  - Architecture description validated

- [ ] **Reviewed by DevOps/Infrastructure**
  - Infrastructure details correct
  - Deployment model accurate
  - Scalability requirements realistic

### Business Review

- [ ] **Reviewed by Product Manager**
  - Product descriptions accurate
  - Customer segments correct
  - Value proposition validated

- [ ] **Reviewed by Business Leader**
  - Strategic objectives current
  - Business model accurate
  - Vision alignment confirmed

### Compliance Review (if applicable)

- [ ] **Reviewed by Legal/Compliance**
  - Regulatory requirements complete
  - Compliance implications correct
  - No legal exposure

---

## 🤖 AI Readiness Test

### Test with AI Tool

Before using widely, test with a small project:

- [ ] **Load Context in AI Tool**
  ```
  "Load [your-context.yaml] for complete business understanding."
  ```

- [ ] **Ask AI to Summarize**
  - AI should accurately summarize your business
  - AI should understand your tech stack
  - AI should respect your constraints

- [ ] **Test with Sample Request**
  ```
  "Based on the business context, recommend a payment
  solution for our mobile app."
  ```
  - Does AI suggest appropriate technology?
  - Does AI respect your constraints (e.g., GDPR)?
  - Does AI consider your existing stack?

- [ ] **Note Gaps**
  - What questions does AI still ask?
  - What context seems missing?
  - What needs clarification?

### Question Tracking

Track questions AI asks that should be in context:

1. _______________________________________________
2. _______________________________________________
3. _______________________________________________
4. _______________________________________________
5. _______________________________________________

**Action**: Add answers to appropriate context sections

---

## 📊 Coverage Assessment

### Business Coverage

- [ ] Who we are (company, history, culture)
- [ ] What we do (products, services, value)
- [ ] Who we serve (customers, segments, markets)
- [ ] How we compete (differentiation, strengths)
- [ ] Where we're going (strategy, vision, objectives)

### Technical Coverage

- [ ] Current technology stack
- [ ] Architecture and patterns
- [ ] Technical constraints
- [ ] Security and compliance
- [ ] Performance and scale requirements

### Operational Coverage

- [ ] How we work (processes, methodology)
- [ ] Decision-making (governance, authority)
- [ ] Partnerships (vendors, integrations)
- [ ] Risks and challenges
- [ ] Success metrics

---

## 🔄 Maintenance Check

### Version Control

- [ ] **File is in Version Control**
  - Committed to git
  - Tagged with version (e.g., v1.0)
  - Change history visible

- [ ] **Metadata Current**
  ```yaml
  metadata:
    document_version: "[current version]"
    last_updated: "[recent date]"
    document_owner: "[current owner]"
  ```

### Review Schedule

- [ ] **Next Review Date Set**
  - Quarterly for fast-changing businesses
  - Semi-annually for most organizations
  - Annually minimum

- [ ] **Update Triggers Defined**
  - Major strategy changes
  - Product launches
  - Organizational changes
  - Technology platform changes
  - Regulatory changes

---

## ✅ Final Sign-Off

### Ready to Use When:

- [ ] All critical sections (Priority 1) complete
- [ ] Quality checks passed
- [ ] Stakeholder reviews complete
- [ ] AI readiness test passed
- [ ] Security/privacy check passed
- [ ] Version controlled

### Sign-Off

- **Completed by**: _____________________
- **Date**: _____________________
- **Version**: _____________________
- **Next Review**: _____________________

---

## 🚀 Post-Validation Actions

Once validated:

1. [ ] **Publish Internally**
   - Share with development team
   - Add to onboarding materials
   - Link from developer docs

2. [ ] **Create Usage Guide**
   - How to reference in AI tools
   - Example prompts
   - Best practices for your team

3. [ ] **Monitor Usage**
   - Track which projects use it
   - Collect feedback
   - Note improvement areas

4. [ ] **Schedule First Review**
   - Set calendar reminder
   - Assign review owner
   - Define review process

---

## 📈 Success Metrics

After 1 month of usage, evaluate:

- [ ] **Time Savings**: Are projects starting faster?
- [ ] **Question Reduction**: Do AI tools ask fewer questions?
- [ ] **Quality Improvement**: Are AI suggestions better?
- [ ] **Team Adoption**: Is team using it consistently?

**If NO to any above**: Review and improve context.

---

## 🆘 Common Issues & Fixes

### Issue: AI Still Asks Too Many Questions

**Fix**:
- Track every question AI asks
- Add answers to context
- Make existing answers more specific
- Ensure context is actually being loaded

### Issue: AI Makes Wrong Assumptions

**Fix**:
- Add explicit constraints (what NOT to do)
- Explain "why" behind decisions more clearly
- Add more context about technical debt/legacy
- Include anti-patterns

### Issue: Context Gets Stale Quickly

**Fix**:
- Set up automated reminders
- Make updating part of project retrospectives
- Assign clear ownership
- Create lightweight update process

### Issue: Too Much Effort to Maintain

**Fix**:
- Focus on critical sections only
- Reduce detail in less important areas
- Automate what you can (metrics, org chart)
- Make updates part of existing processes

---

**Validation Checklist Version**: 1.0.0
**Last Updated**: 2025-11-24
**Created by**: Latentti Oy

---

**Need Help?** See [docs/best-practices.md](../docs/best-practices.md) for guidance on improving your context.
