# /BizContext/fill-section - Fill a Specific Section

When this command is used with a section name/number, execute the following:

## SECTION FILLING WORKFLOW

### Step 1: Load Section Context

1. Identify requested section from argument (e.g., "executive_summary", "1", "technology")
2. Load section definition from current template
3. Load guidance from `.bizcontext-core/data/section-guidance.md`

### Step 2: Explain Section Purpose

Present to user:

```
## Section: {section_name}

**Purpose for AI Development:**
{why_ai_needs_this}

**Critical Fields:**
{list_of_must_have_fields}

**Common Mistakes to Avoid:**
{list_from_anti_patterns}

Let's gather the information. I'll ask questions and challenge any vague answers.
```

### Step 3: Interactive Elicitation

For each critical field:

1. **Ask open-ended question:**
   ```
   {field_name}:
   {question_to_elicit_information}
   ```

2. **Evaluate response immediately:**

   - If SPECIFIC and FACTUAL → Accept and move on
   - If VAGUE → Trigger critique (see Step 4)
   - If MARKETING → Trigger fact-check (see Step 5)

### Step 4: Critique Vague Responses

When response is vague, immediately respond:

```
⚠️ NEEDS MORE SPECIFICITY

You said: "{user_response}"

This isn't specific enough for AI to use. Please provide:
- Exact numbers or ranges
- Time periods
- Comparison points
- Source of information

Example of what I need:
❌ "{vague_version}"
✅ "{specific_version}"

Please try again with more detail:
```

### Step 5: Fact-Check Marketing Language

When response contains marketing language, respond:

```
⚠️ MARKETING LANGUAGE DETECTED

You said: "{user_response}"

Words like "{flagged_words}" don't help AI make development decisions.

Please describe:
1. What evidence supports this claim?
2. How would you prove this to a skeptic?
3. What specific metric measures this?

Transform this:
❌ "{marketing_version}"
✅ "{factual_version}"

Please rephrase with facts:
```

### Step 6: Section Completion

When all critical fields are filled with quality content:

```
✅ Section Complete: {section_name}

Quality Checks Passed:
- [x] All required fields filled
- [x] No placeholder text
- [x] Claims supported by evidence
- [x] No marketing language
- [x] Specific enough for AI use

Progress: {completed}/{total} sections ({percentage}%)

Continue to next section? (yes/no/show status)
```

## SECTION-SPECIFIC GUIDANCE

### Executive Summary
Key questions:
- "What is your exact annual revenue? (range is fine if private)"
- "How many paying customers do you have?"
- "What specific metric proves your competitive advantage?"

### Technology Landscape
Key questions:
- "List every major system with its version and purpose"
- "What technical debt causes the most pain today?"
- "What integrations are critical to daily operations?"

### Constraints & Requirements
Key questions:
- "What regulations must your software comply with?"
- "What's your required system uptime percentage?"
- "What's your budget range for this type of project?"

## SKIP HANDLING

If user wants to skip a section:

```
You want to skip {section_name}.

Options:
1. Skip now, mark for later (recommended)
2. Mark as N/A (not applicable to your business)
3. Fill with minimum viable content

Note: Skipped sections reduce the effectiveness of AI context.
The more complete your document, the better AI can help.

Select 1-3:
```
