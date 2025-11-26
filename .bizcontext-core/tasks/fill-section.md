# Fill Section Task

## Purpose
Guide user through filling a single section of the business context document with high-quality, fact-checked content.

## CRITICAL: Language Rules
- **Accept input in ANY language** - User can describe their business in Finnish, Swedish, German, etc.
- **ALWAYS write to template in ENGLISH** - All YAML content must be in English
- **Respond to user in their language** - Conversation can be in user's preferred language
- **Translate on the fly** - Convert user's input to proper English when writing to template

### Example:
```
User (Finnish): "Meillä on 340 asiakasta, joista 52 on keskisuuria yrityksiä"

Agent response (Finnish): "Hyvä! Kirjoitan templateen englanniksi..."

Written to template (English):
customers: 340
  breakdown:
    mid_market: 52
```

## Execution Flow

### 1. Section Identification
- Accept section name/number from user
- Load section definition from current template
- Load guidance from `data/section-guidance.md` if available

### 2. Section Introduction
Present to user:
```
## {Section Name}

**Why AI Needs This:**
{Explanation of how AI uses this section for development decisions}

**Key Fields to Fill:**
{List of critical fields}

**Quality Standards:**
- Must be specific (numbers, not adjectives)
- Must be factual (evidence, not claims)
- Must be AI-useful (helps development decisions)

**Estimated Time:** {X} minutes

Let's begin. I'll ask questions and challenge any vague answers.
```

### 3. Field-by-Field Elicitation
For each field in the section:

**Ask Question:**
```
{field_name}:
{Open-ended question to elicit information}
```

**Evaluate Response:**

If response is SPECIFIC and FACTUAL:
```
✓ Good: "{response_summary}"

Moving to next field...
```

If response is VAGUE:
```
⚠️ NEEDS SPECIFICITY

You said: "{user_response}"

I need more detail:
- What's the exact number?
- What time period?
- What comparison point?

Example:
❌ "{their_vague_response}"
✅ "{example_specific_response}"

Please provide specifics:
```

If response contains MARKETING LANGUAGE:
```
⚠️ MARKETING LANGUAGE

You said: "{user_response}"

This contains: "{flagged_terms}"

AI can't use adjectives for decisions. Please provide:
- What metric proves this?
- What evidence supports this?
- How would you verify this claim?

Transform:
❌ "{marketing_version}"
✅ "{factual_version}"

Please rephrase with facts:
```

### 4. Section Completion
When all fields are satisfactory:
```
✅ Section Complete: {section_name}

Summary of what we captured:
{Key points summary}

Quality Verification:
- [x] All required fields filled
- [x] Content is specific
- [x] No marketing language
- [x] AI can use this for decisions

Progress: {X}/{Y} sections complete

Options:
1. Continue to next section
2. Review this section again
3. Show current document
4. Take a break (progress saved)

Select 1-4:
```

### 5. Skip Handling
If user wants to skip:
```
You want to skip {field_name}.

Options:
1. Skip now, mark for later
2. Mark as N/A (genuinely not applicable)
3. Provide minimal content

Note: Skipped fields reduce AI effectiveness.
Select 1-3:
```

## Section-Specific Guidance

### executive_summary
Key questions:
- "What's your annual revenue? Even a range is helpful."
- "How many paying customers do you have right now?"
- "What one thing do you do better than any competitor, and how do you prove it?"

Common issues:
- Taglines instead of descriptions
- Missing actual numbers
- Vague market positioning

### technology_landscape
Key questions:
- "List every major system your team uses, with versions."
- "What's your biggest technical pain point right now?"
- "What integrations are critical to daily operations?"

Common issues:
- Technology lists without context
- Hiding legacy systems
- Overstating modernization

### constraints_and_requirements
Key questions:
- "What regulations must your software comply with?"
- "What's your required system uptime? Do you have SLAs?"
- "What's your budget range for a typical project?"

Common issues:
- Generic "must be secure"
- Missing performance requirements
- No budget guidance

## Error Handling

### If user provides no response:
```
I need information for this field to continue.
Options:
1. Provide the information
2. Skip this field (will reduce AI usefulness)
3. Mark as "Unknown" (honest gap)

Select 1-3:
```

### If user is frustrated:
```
I understand this can feel tedious. Here's why it matters:

Generic information like "we have good technology" doesn't help AI
make any specific recommendations. But "PostgreSQL 15 on AWS RDS,
handling 50K transactions/day" tells AI exactly what to work with.

Would you like to:
1. Continue with current section
2. Switch to a different section
3. See examples of good vs bad content
4. Take a break

Select 1-4:
```
