# Business Context Update Template

Structured approach for updating your business context when things change.

---

## 🎯 When to Update

### Immediate Updates Required

Update within 1 week when:
- 🔴 **Major strategy change** (pivot, new direction)
- 🔴 **Large organizational change** (restructure, leadership change)
- 🔴 **Critical technology change** (platform migration, major architecture change)
- 🔴 **New regulatory requirement** (affects all projects)
- 🔴 **Major product launch** (significant new offering)

### Scheduled Updates

- 📅 **Quarterly**: Metrics, strategic objectives, product roadmap
- 📅 **Semi-annually**: Full review of all sections
- 📅 **Annually**: Comprehensive validation and refresh

---

## 📝 Update Process

### Step 1: Identify What Changed

**What triggered this update?**
- [ ] Strategy change
- [ ] Organizational change
- [ ] Technology change
- [ ] Product/service change
- [ ] Market/competitive change
- [ ] Regulatory change
- [ ] Scheduled review
- [ ] AI feedback (questions it shouldn't ask)

**Description of change:**
_____________________________________________
_____________________________________________
_____________________________________________

---

### Step 2: Determine Impact Scope

**Which sections are affected?** (Check all that apply)

- [ ] Section 1: Executive Summary
- [ ] Section 2: Company Profile
- [ ] Section 3: Business History
- [ ] Section 4: Core Business & Value Proposition
- [ ] Section 5: Products and Services
- [ ] Section 6: Customer Segments
- [ ] Section 7: Competitive Landscape
- [ ] Section 8: Business Capabilities
- [ ] Section 9: Business Processes
- [ ] Section 10: Technology Landscape
- [ ] Section 11: Data and Analytics
- [ ] Section 12: Operating Model
- [ ] Section 13: Strategic Objectives
- [ ] Section 14: Success Metrics
- [ ] Section 15: Constraints and Requirements
- [ ] Section 16: Stakeholders
- [ ] Section 17: Partnerships
- [ ] Section 18: Risks and Challenges
- [ ] Section 19: Organizational Culture
- [ ] Section 20: AI Development Context
- [ ] Section 21: Lessons Learned
- [ ] Section 22: Future Vision

---

### Step 3: Make Updates

For each affected section:

#### Section: _____________________

**Current content** (relevant excerpt):
```yaml
[Copy current content here]
```

**Proposed update**:
```yaml
[New content here]
```

**Rationale**:
_____________________________________________
_____________________________________________

**Validated by**: _______________ Date: ___________

---

### Step 4: Update Metadata

```yaml
metadata:
  document_version: "[increment version - e.g., 1.0 → 1.1]"
  last_updated: "[today's date YYYY-MM-DD]"
  document_owner: "[current owner]"
  review_frequency: "[unchanged or updated]"

version_history:
  - version: "[new version]"
    date: "[today's date]"
    changes: "[summary of changes]"
    author: "[your name]"
```

---

### Step 5: Validation

**Review checklist:**
- [ ] All updates are accurate
- [ ] No new placeholder text
- [ ] Specific, not generic
- [ ] Numbers and metrics current
- [ ] Contradictions resolved
- [ ] Cross-references updated
- [ ] YAML syntax valid

**Stakeholder review:**
- [ ] Technical review (if tech changes)
- [ ] Business review (if strategy changes)
- [ ] Compliance review (if regulations changed)

---

### Step 6: Commit and Communicate

**Git commit:**
```bash
git add [your-context-file].yaml
git commit -m "Update business context v[X.Y]

[Brief description of changes]

Updated sections:
- Section X: [change]
- Section Y: [change]

Triggered by: [what changed]"

git tag business-context-v[X.Y]
git push && git push --tags
```

**Communication:**
- [ ] Notify development team
- [ ] Update any copies/references
- [ ] Announce in team channel
- [ ] Update documentation links (if needed)

---

## 📋 Common Update Scenarios

### Scenario 1: Quarterly Metrics Update

**Sections to update:**
- Section 1: Executive Summary (key metrics)
- Section 14: Success Metrics (all metrics)
- Section 5: Products (user counts, revenue)

**Checklist:**
- [ ] Financial metrics (revenue, growth)
- [ ] Customer metrics (count, churn, NPS)
- [ ] Product metrics (users, adoption)
- [ ] Operational metrics (uptime, performance)

**Estimated time**: 30-60 minutes

---

### Scenario 2: New Product Launch

**Sections to update:**
- Section 1: Executive Summary (add to portfolio)
- Section 5: Products and Services (new product detail)
- Section 6: Customer Segments (if new segment)
- Section 13: Strategic Objectives (if supports new objective)
- Section 22: Future Vision (update roadmap)

**Checklist:**
- [ ] Product description and features
- [ ] Target customers and segments
- [ ] Pricing model
- [ ] Business metrics goals
- [ ] Competitive positioning
- [ ] Integration with existing products

**Estimated time**: 2-4 hours

---

### Scenario 3: Major Technology Migration

**Sections to update:**
- Section 10: Technology Landscape (new tech stack)
- Section 15: Constraints (new/removed constraints)
- Section 21: Lessons Learned (why migrating)

**Checklist:**
- [ ] Update current technology stack
- [ ] Note legacy systems being replaced
- [ ] Add migration timeline
- [ ] Update architecture style (if changed)
- [ ] Document new constraints
- [ ] Update technology principles (if changed)
- [ ] Add lessons learned from old system

**Estimated time**: 2-3 hours

---

### Scenario 4: Organizational Restructure

**Sections to update:**
- Section 2: Company Profile (org structure)
- Section 12: Operating Model (if model changed)
- Section 16: Stakeholders (new decision makers)

**Checklist:**
- [ ] Update org chart/structure
- [ ] Update leadership team
- [ ] Update department descriptions
- [ ] Update decision-making authority
- [ ] Update governance bodies
- [ ] Note culture changes (if any)

**Estimated time**: 1-2 hours

---

### Scenario 5: Strategic Pivot

**Sections to update:**
- Section 1: Executive Summary (vision, mission)
- Section 4: Core Business (value proposition)
- Section 13: Strategic Objectives (new objectives)
- Section 22: Future Vision (new direction)
- Section 7: Competitive Landscape (if positioning changed)

**Checklist:**
- [ ] Update vision and mission
- [ ] Revise strategic objectives
- [ ] Update value proposition
- [ ] Note what's changing vs. staying same
- [ ] Update market positioning
- [ ] Revise future vision
- [ ] Add to business history (Section 3)

**Estimated time**: 4-6 hours

---

### Scenario 6: New Regulatory Requirement

**Sections to update:**
- Section 15: Constraints (new regulations)
- Section 18: Risks (compliance risks)
- Section 10: Technology (if tech impact)

**Checklist:**
- [ ] Document new regulation
- [ ] State applicability
- [ ] List specific requirements
- [ ] Explain implications for AI development
- [ ] Note compliance deadline
- [ ] Update risk assessment
- [ ] Add technology constraints (if any)

**Estimated time**: 1-2 hours

---

## 🔄 Version Numbering Guide

Use semantic versioning for your business context:

**Major version (X.0.0)**: Breaking changes
- Complete restructure
- Major strategic pivot
- Fundamentally different business

**Minor version (1.X.0)**: Significant additions
- New major product line
- Significant org change
- New market entry
- Major tech migration

**Patch version (1.0.X)**: Small updates
- Metrics refresh
- Minor product updates
- Small corrections
- Clarifications

---

## 📊 Update Log Template

Keep a change log in your context file:

```yaml
update_log:
  - version: "1.2.0"
    date: "2025-03-15"
    type: "Minor"
    trigger: "New product launch"
    sections_updated:
      - "Section 5: Added AI Analytics product"
      - "Section 13: Updated strategic objectives"
    author: "John Doe"
    review_date: "2025-03-16"

  - version: "1.1.1"
    date: "2025-01-15"
    type: "Patch"
    trigger: "Quarterly metrics update"
    sections_updated:
      - "Section 1: Updated key metrics"
      - "Section 14: Refreshed all metrics"
    author: "Jane Smith"
    review_date: "2025-01-15"
```

---

## ✅ Post-Update Checklist

After making updates:

- [ ] **Test with AI tool**
  - Load updated context
  - Verify AI understands changes
  - Note any confusion

- [ ] **Notify team**
  - Send update notification
  - Highlight key changes
  - Remind where to find it

- [ ] **Update documentation**
  - Developer onboarding docs
  - Project templates
  - Team wiki/knowledge base

- [ ] **Schedule next review**
  - Based on review frequency
  - Set calendar reminder
  - Assign owner

---

## 🆘 Rollback Procedure

If an update causes problems:

```bash
# View recent commits
git log --oneline -5

# Rollback to previous version
git revert [commit-hash]

# Or restore specific version
git checkout [tag-name] -- [your-context.yaml]

# Create rollback commit
git commit -m "Rollback to v[X.Y] due to [reason]"
git push
```

**Then**:
1. Notify team of rollback
2. Investigate what went wrong
3. Fix issues in new update
4. Re-apply carefully

---

## 💡 Tips for Smooth Updates

### Keep It Fresh
- Don't let context get more than 6 months out of date
- Small frequent updates better than large infrequent ones
- Make updating part of normal workflow

### Get Input
- Ask developers what they wish context included
- Track questions AI shouldn't need to ask
- Review usage feedback regularly

### Stay Organized
- Use consistent format for updates
- Keep change log current
- Tag versions clearly

### Test Before Publishing
- Test updated context with AI
- Verify no regressions
- Get stakeholder sign-off

---

## 📞 Need Help?

**If update is complex:**
- Review [docs/usage-guide.md](../docs/usage-guide.md)
- Check [docs/best-practices.md](../docs/best-practices.md)
- Open a discussion on GitHub
- Email: ari.hietamaki@latentti.fi

---

**Update Template Version**: 1.0.0
**Last Updated**: 2025-11-24
**Created by**: Latentti Oy
