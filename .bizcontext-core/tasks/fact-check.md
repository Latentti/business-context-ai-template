# Fact-Check Task

## Purpose
Evaluate content for factual accuracy, specificity, and AI-usefulness. Challenge claims that lack evidence.

## Execution Flow

### 1. Receive Content
Accept content to fact-check:
- A specific field value
- A section of the document
- User-provided text

### 2. Pattern Detection
Scan for red flag patterns:

```yaml
patterns_to_flag:
  superlatives:
    words: [best, leading, top, premier, world-class, industry-leading, cutting-edge, innovative]
    action: "Demand supporting metric"

  vague_quantities:
    words: [many, several, few, some, significant, substantial, numerous, various]
    action: "Request exact number"

  marketing_buzzwords:
    words: [synergy, leverage, optimize, holistic, seamless, robust, scalable, agile, dynamic]
    action: "Request concrete description"

  opinion_markers:
    phrases: [we believe, we think, we feel, is considered, is known for, is recognized]
    action: "Request verifiable fact"

  future_promises:
    phrases: [will be, planning to, working on, soon, in the future, roadmap includes]
    action: "Clarify current state vs planned"

  hedge_words:
    words: [approximately, around, roughly, about, nearly, almost]
    action: "Request exact or range"
```

### 3. Issue Report
For each issue found:

```
🔍 FACT-CHECK RESULT

**Content Analyzed:**
"{content}"

**Issues Found:** {count}

---

### Issue 1: {pattern_type}
**Found:** "{flagged_text}"
**Problem:** {why_this_is_problematic}
**Required:** {what_is_needed}

**Example Fix:**
❌ Current: "{current_text}"
✅ Better: "{improved_text}"

---

### Issue 2: ...

---

**Overall Assessment:** {PASS / NEEDS_EVIDENCE / MARKETING_FLUFF}

Would you like to:
1. Provide the requested evidence for each issue
2. Acknowledge these as gaps (honest "unknown")
3. Challenge my assessment

Select 1-3:
```

### 4. Resolution Loop
For each issue, guide to resolution:

```
Let's fix Issue {N}: {issue_description}

Current text: "{problematic_text}"

I need:
{specific_information_needed}

Your response:
```

Repeat until resolved or acknowledged as gap.

## Fact-Check Questions by Type

### For Superlatives
- "What metric supports 'leading'? Market share?"
- "According to what source?"
- "Compared to which competitors?"
- "As of what date?"

### For Vague Quantities
- "What's the exact number?"
- "If you don't know exact, what's the range?"
- "Over what time period?"
- "How is this measured?"

### For Market Position Claims
- "What's your market share percentage?"
- "Source of market data?"
- "Which specific market/segment?"
- "As of when?"

### For Technology Claims
- "What specific version?"
- "How is it deployed?"
- "What scale?"
- "What's the actual technical debt?"

### For Performance Claims
- "What's the measured performance?"
- "Over what time period?"
- "Under what conditions?"
- "What monitoring tracks this?"

## Severity Levels

### Critical (Must Fix)
- Claims that would mislead AI development
- Constraints stated vaguely (security, compliance)
- Technology descriptions that don't match reality

### High (Should Fix)
- Marketing language in key sections
- Missing metrics for business decisions
- Vague competitive positioning

### Medium (Recommended Fix)
- Imprecise quantities
- Minor buzzwords
- Hedge words

### Low (Nice to Fix)
- Stylistic issues
- Minor precision improvements
- Format inconsistencies

## Output Format

```
# FACT-CHECK SUMMARY

**Document/Section:** {name}
**Content Length:** {size}
**Check Date:** {timestamp}

## Issues by Severity

**Critical ({count}):**
- {issue}: {location}

**High ({count}):**
- {issue}: {location}

**Medium ({count}):**
- {issue}: {location}

**Low ({count}):**
- {issue}: {location}

## Detailed Findings
{Full issue descriptions with fixes}

## Next Steps
1. {Priority fix 1}
2. {Priority fix 2}
3. {Priority fix 3}
```
