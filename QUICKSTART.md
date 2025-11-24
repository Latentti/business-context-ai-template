# Quick Start Guide

Get your business context up and running in 30 minutes to 6 hours, depending on your needs.

---

## 🚀 Super Quick Start (30 minutes)

Want to try this out RIGHT NOW? Here's the absolute fastest path:

### 1. Copy the Quick Start Template (2 min)

```bash
cd business-context-ai-template/templates
cp business-context-quickstart.yaml my-company.yaml
```

### 2. Fill Out Executive Summary (10 min)

Open `my-company.yaml` and fill Section 1:

```yaml
executive_summary:
  company_name: "YourCompany Inc"
  tagline: "What you do in one sentence"
  key_metrics:
    annual_revenue: "$5M"
    customers: "1000"
    employees: "25"
  competitive_advantage: "Why customers choose you"
  vision_3_5_years: "Where you want to be"
```

### 3. Add Your Tech Stack (10 min)

Fill Section 4:

```yaml
core_technologies:
  frontend: "React"
  backend: "Node.js/Express"
  database: "PostgreSQL"
  cloud_infrastructure: "AWS"
```

### 4. Note Your Main Constraints (5 min)

Fill Section 5:

```yaml
regulatory_compliance:
  - regulation: "GDPR"
    requirements: "User data protection, consent management"

security_requirements:
  - "All API calls must use authentication"
  - "Encryption at rest and in transit"
```

### 5. Use It! (3 min)

In your next AI project:

```
"Load my-company.yaml for business context. Build a [feature]..."
```

**Done!** You have a minimal viable business context.

---

## 📊 Standard Quick Start (4-6 hours)

For a more complete context that covers the essentials:

### Step 1: Choose Template (5 min)

```bash
cd business-context-ai-template/templates

# For startups/small companies
cp business-context-quickstart.yaml ../my-company.yaml

# For mid-size companies
cp business-context-full.yaml ../my-company.yaml
```

### Step 2: Gather Materials (30 min)

Before you start filling, collect:

- [ ] Company strategy documents
- [ ] Product/service descriptions
- [ ] Tech architecture docs or diagrams
- [ ] Organizational chart
- [ ] Key metrics (customers, revenue, etc.)
- [ ] Compliance requirements

### Step 3: Fill Priority 1 Sections (2-3 hours)

**Required sections** - AI needs these to function:

#### Section 1: Executive Summary (30 min)
```yaml
company_name: "Your Company"
tagline: "One-sentence description"
key_metrics:
  annual_revenue: "[Number]"
  employees: "[Number]"
  customers: "[Number]"
competitive_advantage: "Specific differentiator"
vision_3_5_years: "Where you're heading"
```

#### Section 4: Core Business (45 min)
```yaml
elevator_pitch: "30-second description"
value_proposition:
  primary_value: "Core value you deliver"
  why_customers_choose_you:
    reason_1: "Specific reason"
    reason_2: "Specific reason"
```

#### Section 5: Products (1 hour)
```yaml
product_1:
  name: "Product Name"
  description: "What it does and for whom"
  key_features:
    - "Feature 1"
    - "Feature 2"
  business_metrics:
    users: "[Number]"
    revenue_contribution: "[Percentage]"
```

#### Section 10: Technology (1 hour)
```yaml
core_technologies:
  frontend: "Your frontend tech"
  backend: "Your backend tech"
  database: "Your database"
  infrastructure: "Cloud provider"

architecture_style: "Microservices/Monolithic/etc"
```

#### Section 15: Constraints (30 min)
```yaml
regulatory_compliance:
  - regulation: "GDPR/HIPAA/etc"
    requirements: "What you must do"

security_requirements:
  - "Specific security requirement"

performance_requirements:
  - "SLA or performance target"
```

### Step 4: Validate (30 min)

- [ ] Have tech lead review Section 10 (Technology)
- [ ] Have business lead review Sections 1, 4, 5
- [ ] Check for placeholder text
- [ ] Verify numbers are accurate

### Step 5: Version Control (5 min)

```bash
git add my-company.yaml
git commit -m "Add business context v1.0"
git tag business-context-v1.0
```

### Step 6: Use In Project (5 min)

```
"Before we start this project, read my-company.yaml for complete
business context. Pay special attention to:
- Section 10 (Technology Stack)
- Section 15 (Constraints)

Now for THIS specific project: [details]"
```

---

## 🏢 Enterprise Quick Start (2-4 days)

For larger organizations needing comprehensive coverage:

### Phase 1: Planning (4 hours)
- Identify stakeholders
- Schedule working sessions
- Assign section owners
- Gather existing documentation

### Phase 2: Core Content (1-2 days)
- Leadership team: Strategy, vision, business model
- Product team: Products, customers, value proposition
- Technology team: Architecture, stack, constraints
- Operations team: Processes, workflows

### Phase 3: Review & Validate (4-6 hours)
- Cross-functional review
- Stakeholder validation
- Consistency check
- Gap identification

### Phase 4: Finalize (2-4 hours)
- Incorporate feedback
- Final review
- Publish internally
- Communication plan

---

## ⚡ What You Get

After completing this quick start:

### Immediate Benefits
- ✅ Stop explaining same business context in every project
- ✅ AI makes decisions aligned with your business
- ✅ Faster project starts (hours → minutes)
- ✅ Consistent quality across projects

### Tangible Results
- **Before**: "Build a payment feature" → 2-4 hours of Q&A
- **After**: "Load context.yaml. Build payment feature" → 5 minutes of Q&A

### Time Savings
- **Per project**: Save 2-4 hours in briefing
- **10 projects/year**: Save 20-40 hours
- **100 projects/year**: Save 200-400 hours

---

## 🎯 Next Steps

Once you have a working business context:

### Week 1: Test & Iterate
- Use in 2-3 projects
- Note what questions AI still asks
- Refine your context

### Month 1: Expand
- Add Priority 2 sections
- Fill gaps discovered during use
- Get more stakeholder input

### Quarter 1: Establish Process
- Schedule quarterly reviews
- Assign document owner
- Create update workflow
- Train team on usage

### Ongoing: Maintain
- Update after major changes
- Review quarterly
- Keep metrics current
- Expand as needed

---

## 💡 Tips for Success

### Do's ✅
- **Start simple** - Don't try to be perfect initially
- **Use in projects immediately** - Learn what's missing
- **Be specific** - Numbers, names, versions
- **Be honest** - Include technical debt and constraints
- **Iterate** - Improve over time

### Don'ts ❌
- **Don't wait for perfection** - Done is better than perfect
- **Don't work alone** - Get input from team
- **Don't be vague** - AI needs specifics
- **Don't hide problems** - Technical debt is real
- **Don't forget to maintain** - Context gets stale

---

## 🆘 Troubleshooting

### "I don't know what to write for Section X"

**Solution**:
1. Skip it for now (mark as "TBD")
2. Fill what you know
3. Come back later
4. Or mark as "N/A" if truly not applicable

### "This is taking too long"

**Solution**:
1. Use Quick Start template (not Full)
2. Fill only Priority 1 sections
3. Spread work over multiple sessions
4. Get help from teammates

### "My business is too complex for this"

**Solution**:
1. Start with one business unit
2. Create master + BU-specific contexts
3. Use Enterprise template
4. Focus on what's most important first

### "AI still asks too many questions"

**Solution**:
1. Note the questions AI asks
2. Add those answers to your context
3. Be more specific in relevant sections
4. Iterate and improve

---

## 📚 Additional Resources

- **[Full Usage Guide](docs/usage-guide.md)** - Detailed instructions
- **[Best Practices](docs/best-practices.md)** - How to write effective context
- **[Examples](examples/)** - See filled examples
- **[FAQ](docs/faq.md)** - Common questions

---

## 🎉 Success Stories

> "We went from 3 hours of briefing per project to 15 minutes. Saved our team 40+ hours per month."
> — Tech Lead, SaaS Startup

> "Our AI suggestions are now actually usable because they respect our architecture constraints."
> — Principal Engineer, Enterprise

> "Finally, a way to onboard new developers that doesn't require hours of meetings."
> — Engineering Manager, Scale-up

---

**Ready to save hours on every AI project? Pick a Quick Start path above and begin!**

[← Back to README](README.md) | [Full Usage Guide →](docs/usage-guide.md)
