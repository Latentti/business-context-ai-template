# /BizContext/validate - Validate Complete Document

When this command is used, execute comprehensive validation of the business context document.

## VALIDATION WORKFLOW

### Step 1: Load Document

```
🔍 Starting Full Document Validation

Loading: {document_path}
Template type: {quickstart/full/enterprise}
Sections to validate: {count}

This validation checks:
✓ Completeness - all required fields filled
✓ Quality - content meets AI-usefulness standards
✓ Consistency - information doesn't contradict itself
✓ Specificity - claims are backed by data

Beginning validation...
```

### Step 2: Section-by-Section Validation

For each section, run these checks:

#### Completeness Check
```yaml
section: {section_name}
completeness:
  required_fields: {count}
  filled_fields: {count}
  empty_fields:
    - {field_name}: "Missing"
  placeholder_text_found:
    - {field}: "{placeholder_text}"
  status: {COMPLETE / INCOMPLETE}
```

#### Quality Check
```yaml
section: {section_name}
quality:
  ai_usefulness: {1-5}
  specificity: {1-5}
  factual_accuracy: {1-5}
  issues:
    - type: {issue_type}
      field: {field_name}
      problem: "{description}"
      suggestion: "{improvement}"
  status: {PASS / NEEDS_WORK / FAIL}
```

#### Consistency Check
```yaml
cross_reference_issues:
  - fields: ["{field1}", "{field2}"]
    issue: "{description of contradiction}"
    resolution: "{suggested fix}"
```

### Step 3: Generate Validation Report

```markdown
# 📋 VALIDATION REPORT

**Document:** {filename}
**Template:** {template_type}
**Validated:** {timestamp}

---

## OVERALL SCORE: {score}/100

| Category | Score | Status |
|----------|-------|--------|
| Completeness | {x}/100 | {✅/⚠️/❌} |
| Quality | {x}/100 | {✅/⚠️/❌} |
| Specificity | {x}/100 | {✅/⚠️/❌} |
| Consistency | {x}/100 | {✅/⚠️/❌} |

---

## SECTION SUMMARY

| Section | Complete | Quality | Issues |
|---------|----------|---------|--------|
| {section_1} | {yes/no} | {1-5} | {count} |
| {section_2} | {yes/no} | {1-5} | {count} |
...

---

## CRITICAL ISSUES ({count})

Issues that must be fixed before document is AI-ready:

### Issue 1: {title}
- **Section:** {section}
- **Field:** {field}
- **Problem:** {description}
- **Impact:** {why this matters for AI}
- **Fix:** {specific suggestion}

### Issue 2: {title}
...

---

## WARNINGS ({count})

Issues that reduce document effectiveness:

### Warning 1: {title}
- **Section:** {section}
- **Problem:** {description}
- **Recommendation:** {suggestion}

---

## PASSED CHECKS ({count})

✅ {list of things that passed validation}

---

## RECOMMENDATIONS

1. **Priority 1:** {most important improvement}
2. **Priority 2:** {second improvement}
3. **Priority 3:** {third improvement}

---

## AI-READINESS VERDICT

{READY / NEEDS_WORK / NOT_READY}

{Explanation of verdict and next steps}
```

### Step 4: Offer Fix Assistance

```
Validation complete. What would you like to do?

1. Fix critical issues now (interactive)
2. Fix all issues automatically (AI-suggested fixes)
3. Export validation report
4. Show detailed issues for a specific section
5. Re-validate after manual fixes

Select 1-5:
```

## VALIDATION RULES

### Completeness Rules
- All fields marked as required must have values
- No placeholder text (e.g., "[Your company]", "TBD", "TODO")
- No empty arrays or objects where content is expected

### Quality Rules
- Executive summary must have at least 3 quantified metrics
- Technology landscape must list specific systems with versions
- Constraints must include measurable requirements
- Strategy sections must have timeframes

### Specificity Rules
- Numbers > adjectives (flag vague quantities)
- Metrics > claims (flag unverified statements)
- Evidence > opinion (flag "we believe" type statements)

### Consistency Rules
- Employee count should be consistent across sections
- Revenue figures should align
- Technology mentions should be consistent
- Timeline references should not contradict

## SCORING METHODOLOGY

```
Completeness Score:
- Start with 100
- -10 per missing required field
- -5 per placeholder text found
- Minimum: 0

Quality Score:
- Start with 100
- -15 per marketing language instance
- -10 per vague claim
- -5 per missing evidence
- Minimum: 0

Specificity Score:
- Start with 100
- -10 per vague quantity
- -10 per missing metric
- -5 per superlative without data
- Minimum: 0

Consistency Score:
- Start with 100
- -20 per contradiction found
- -10 per inconsistent reference
- Minimum: 0

Overall = (Completeness + Quality + Specificity + Consistency) / 4
```

## AI-READINESS THRESHOLDS

- **READY** (80+): Document can be used effectively for AI development
- **NEEDS_WORK** (50-79): Document is usable but with reduced effectiveness
- **NOT_READY** (<50): Document needs significant improvement before use
