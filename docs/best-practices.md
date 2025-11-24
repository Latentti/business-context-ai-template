# Best Practices - Business Context for AI

Learn how to write effective business context that AI can actually use.

---

## Table of Contents

1. [Core Principles](#core-principles)
2. [Writing for AI vs. Humans](#writing-for-ai-vs-humans)
3. [Common Patterns](#common-patterns)
4. [Anti-Patterns to Avoid](#anti-patterns-to-avoid)
5. [Section-Specific Tips](#section-specific-tips)
6. [Real Examples](#real-examples)

---

## Core Principles

### 1. **Specificity Over Generality**

AI cannot infer meaning from vague descriptions. Be concrete.

#### ❌ BAD:
```yaml
competitive_advantage: "We provide great service and innovative solutions"
```

#### ✅ GOOD:
```yaml
competitive_advantage:
  core_differentiator: "While competitors pilot AI in labs, we run AI at production
   scale: 20M transactions/year through ML decision engine with 99.97% uptime.
   Customer implementations in 6 weeks vs industry average 6 months."

  proof_points:
    - "500K+ active users on AI-powered platform"
    - "2B+ events/year processed by ML models"
    - "43% faster time-to-value than nearest competitor (verified by Gartner)"
```

**Why it matters**: AI can make better decisions when it understands *specifically* what makes you different.

---

### 2. **Quantify Everything**

Numbers are unambiguous. Use them liberally.

#### ❌ BAD:
```yaml
company_size: "We're a growing mid-size company"
performance: "Our system is fast and reliable"
```

#### ✅ GOOD:
```yaml
company_metrics:
  employees: 247
  annual_revenue: "$42M (FY2024)"
  customers: 1834
  yoy_growth: "38%"

performance_requirements:
  api_response_time: "< 200ms P95, < 500ms P99"
  system_uptime: "99.97% (< 2.6 hours downtime/year)"
  throughput: "5000 requests/second sustained, 15000 burst"
```

**Why it matters**: AI can make trade-offs and design decisions based on actual numbers.

---

### 3. **Explain the "Why"**

AI needs context for decisions, not just what you do.

#### ❌ BAD:
```yaml
database: "PostgreSQL"
```

#### ✅ GOOD:
```yaml
database_standard: "PostgreSQL for all ACID-compliant data"

rationale: "Standardized on PostgreSQL after 2021 incident where MySQL
 replication lag caused $50K in financial discrepancies affecting 10,000
 customers. PostgreSQL's synchronous replication and proven ACID compliance
 are non-negotiable for financial systems.

alternatives_and_context:
  mongodb: "Used only for non-critical logging and caching where eventual
    consistency is acceptable. NEVER for financial or customer personal data."
  mysql: "Being phased out. No new projects. Existing instances migrating to
    PostgreSQL by Q3 2025."
```

**Why it matters**: AI won't accidentally suggest MySQL for financial data when it understands the history.

---

### 4. **Include Constraints and Boundaries**

Tell AI what NOT to do, not just what to do.

#### ❌ BAD:
```yaml
security: "We take security seriously"
```

#### ✅ GOOD:
```yaml
security_requirements:
  data_classification:
    pii_handling:
      requirement: "All PII must be encrypted at rest (AES-256) and in transit (TLS 1.3+)"
      prohibited: "NEVER store PII in logs, error messages, or analytics tools"
      violation_consequence: "Regulatory fine up to €20M under GDPR"

    payment_data:
      requirement: "PCI-DSS Level 1 compliance mandatory"
      approach: "Tokenization via Stripe - never store card numbers"
      prohibited: "NEVER handle raw card data in our systems"

  authentication:
    required: "MFA mandatory for all admin access"
    prohibited: "No password-only authentication for production systems"
```

**Why it matters**: AI won't accidentally create security violations when boundaries are clear.

---

### 5. **Show, Don't Just Tell**

Provide examples, not just descriptions.

#### ❌ BAD:
```yaml
customer_segments: "We serve various types of businesses"
```

#### ✅ GOOD:
```yaml
customer_segments:
  enterprise:
    definition: "Companies with 500+ employees, $50M+ revenue"

    examples:
      - name: "Acme Corp"
        industry: "Manufacturing"
        employees: 2500
        use_case: "Supply chain optimization"
        pain_point: "Manual forecasting caused $5M in excess inventory"
        our_solution: "AI-powered demand forecasting reduced excess by 40%"
        contract_value: "$450K/year"

      - name: "Global Bank (NDA)"
        industry: "Financial Services"
        employees: 15000
        use_case: "Fraud detection"
        pain_point: "14% false positive rate costing $2M/year in investigations"
        our_solution: "ML models reduced false positives to 3%"
        contract_value: "$1.2M/year"

    common_patterns:
      - "Need SOC 2 Type II compliance"
      - "Require on-premise deployment option"
      - "9-18 month sales cycles"
      - "Multiple stakeholder approval (IT, Legal, Procurement, Business)"
```

**Why it matters**: Concrete examples help AI understand patterns and make analogies.

---

## Writing for AI vs. Humans

### Human Documentation
- Marketing-friendly language
- High-level vision and aspirations
- Storytelling and narrative
- Assumes shared context
- Room for interpretation

### AI Context
- Precise, unambiguous language
- Specific facts and constraints
- Structured data
- Assumes zero prior context
- Explicit, not implicit

---

### Example Comparison

#### Marketing Copy (Human-focused):
> "Acme revolutionizes enterprise workflows with cutting-edge AI that empowers teams to achieve unprecedented productivity gains and unlock transformative business value."

#### AI Context (AI-focused):
```yaml
product_description:
  name: "Acme Workflow Engine"
  category: "Enterprise Workflow Automation Platform"

  core_functionality: "Automates repetitive business processes using ML-powered
    document extraction, decision routing, and process optimization."

  target_users: "Knowledge workers in enterprise back-office operations
    (finance, HR, procurement)"

  quantified_value:
    time_savings: "Average 12 hours/week per user (verified across 150 customers)"
    error_reduction: "87% reduction in manual data entry errors"
    roi: "Positive ROI within 4.2 months (median customer)"

  technical_implementation:
    deployment: "SaaS (AWS) or On-premise (customer infrastructure)"
    integration_methods: "REST API, Webhooks, Pre-built connectors (Salesforce, SAP, Workday)"
    ml_models: "Document classification (BERT-based), Entity extraction (custom NER)"
```

**Key differences:**
- ❌ "Revolutionary", "cutting-edge", "unprecedented" → ✅ Specific capabilities
- ❌ "Empowers teams" → ✅ Quantified value (12 hours/week)
- ❌ "Transformative business value" → ✅ Measurable ROI (4.2 months)

---

## Common Patterns

### Pattern 1: Technology Choices

Always explain technology selections:

```yaml
technology_choices:
  choice: "React Native for mobile apps"

  rationale:
    - "Single codebase reduces development cost 40% vs native"
    - "Faster iteration (hot reload, shared business logic)"
    - "95% code reuse between iOS and Android"
    - "Team expertise: 8/12 developers know React, only 2 know Swift/Kotlin"

  trade_offs_accepted:
    performance: "10-15% slower than native for complex animations - acceptable
      for our use case (form-based app, not gaming)"
    native_features: "Some platform-specific features require bridges - worth
      it for development speed"

  alternatives_considered:
    flutter: "Rejected - team has no Dart experience, training cost too high"
    native: "Rejected - can't afford separate iOS and Android teams"
```

---

### Pattern 2: Regulatory Compliance

Be specific about requirements and implications:

```yaml
regulatory_compliance:
  regulation: "GDPR (General Data Protection Regulation)"

  applicability: "All customer data - we process PII for 500K EU citizens"

  specific_requirements:
    consent:
      requirement: "Explicit opt-in consent required for data processing"
      implementation: "Consent management system with granular controls"
      ai_implication: "All data collection features must include consent flow"

    right_to_deletion:
      requirement: "Delete all personal data within 30 days of request"
      implementation: "Automated deletion workflow across all systems"
      ai_implication: "Soft deletes only - no hard foreign key constraints that
        prevent deletion"

    data_portability:
      requirement: "Provide user data in machine-readable format"
      implementation: "Export to JSON via API"
      ai_implication: "All user data must be queryable via single user_id"

  violations_consequence:
    fine: "Up to €20M or 4% of global revenue, whichever is higher"
    reputation: "Public disclosure of violations - brand damage"

  ai_development_impact:
    - "NEVER store PII in logs or error messages"
    - "All analytics must anonymize or pseudonymize data"
    - "Features must work with minimal data collection"
    - "Data retention: 90 days max for non-essential data"
```

---

### Pattern 3: Customer Segments

Provide rich, specific customer profiles:

```yaml
customer_segments:
  segment_name: "Mid-Market SaaS Companies"

  profile:
    company_size: "50-500 employees"
    revenue: "$5M-$50M ARR"
    industry: "B2B SaaS"
    geography: "North America primary, expanding to Europe"

  decision_makers:
    primary: "VP of Engineering or CTO"
    influencers: "Engineering team leads, DevOps engineers"
    approval_authority: "Usually under $50K, CTO can approve. Over $50K needs CFO."

  pain_points:
    primary_pain:
      description: "Scaling development team while maintaining code quality"
      impact: "Shipping velocity decreased 30% as team grew from 10 to 40 engineers"
      current_solution: "Manual code reviews causing 2-day merge delays"
      cost_of_problem: "$500K/year in delayed features and lost revenue"

    secondary_pain:
      description: "Technical debt accumulating faster than can pay down"
      impact: "Estimated 40% of codebase needs refactoring"

  buying_behavior:
    sales_cycle: "30-60 days"
    evaluation_process:
      - "2-week free trial with real code"
      - "Security review (if >$25K contract)"
      - "Reference calls with similar companies"
    decision_criteria:
      - must_have: "Supports our tech stack (React/Node.js/PostgreSQL)"
      - must_have: "SOC 2 Type II certified"
      - nice_to_have: "Integrates with GitHub Enterprise"
      - deal_breaker: "Requires changing our CI/CD pipeline"

  segment_metrics:
    total_customers: 234
    revenue_contribution: "42% of total revenue"
    ltv: "$125K"
    cac: "$18K"
    ltv_cac_ratio: "7:1"
    churn_rate: "8% annual"
    nps: "+62"
```

---

## Anti-Patterns to Avoid

### Anti-Pattern 1: Buzzword Bingo

❌ **Bad**:
```yaml
about_us: "We're a disruptive, innovative, cutting-edge, next-generation,
  AI-powered, blockchain-enabled, paradigm-shifting platform revolutionizing
  the enterprise landscape with synergistic solutions that leverage big data
  and machine learning to drive digital transformation."
```

✅ **Good**:
```yaml
about_us:
  what_we_do: "Enterprise workflow automation platform that uses ML to extract
    data from documents and route tasks to appropriate teams."

  how_we_do_it:
    - "Document classification using BERT-based models (94% accuracy)"
    - "Named entity extraction for key data fields"
    - "Rule-based + ML-powered routing engine"
    - "Integration with existing enterprise systems (SAP, Salesforce, etc.)"

  results:
    - "Average 12 hours/week saved per user"
    - "87% reduction in manual data entry errors"
    - "Deployed at 150 enterprise customers"
```

---

### Anti-Pattern 2: Hiding Problems

❌ **Bad** (pretending you have no technical debt):
```yaml
technology_landscape: "Modern, cloud-native microservices architecture"
```

✅ **Good** (honest about reality):
```yaml
technology_landscape:
  architecture: "Hybrid - migrating from monolith to microservices"

  current_state:
    monolith:
      description: "PHP/Laravel monolith ('the Legacy App')"
      percentage_of_traffic: "60%"
      status: "Maintenance mode - no new features"
      technical_debt: "HIGH - minimal test coverage, PHP 7.4 (EOL soon)"
      migration_plan: "Strangler fig pattern - new features in microservices"
      timeline: "Full migration Q4 2026"

    microservices:
      description: "Node.js/Express microservices"
      percentage_of_traffic: "40% and growing"
      services_count: 12
      status: "Active development - all new features here"
      tech_stack: "Node.js 20 LTS, PostgreSQL, Redis, RabbitMQ"

  implications_for_ai:
    - "New features: Build in microservices (Node.js)"
    - "Bug fixes in monolith: Touch legacy code minimally"
    - "Integration: Must work with both architectures"
    - "Testing: Legacy app has minimal tests - be extra careful"
```

**Why honesty matters**: AI will make better recommendations when it knows the real constraints.

---

### Anti-Pattern 3: Generic Requirements

❌ **Bad**:
```yaml
performance: "The system should be fast"
security: "We need good security"
scalability: "It must scale well"
```

✅ **Good**:
```yaml
performance_requirements:
  api_latency:
    p50: "< 100ms"
    p95: "< 200ms"
    p99: "< 500ms"
    measurement: "Measured at load balancer, includes database queries"
    consequence_if_missed: "Customer SLA violation, potential refund"

  page_load_time:
    target: "< 2 seconds for First Contentful Paint"
    measurement: "Real user monitoring (RUM) via DataDog"
    current: "2.8 seconds (needs optimization)"

  database_queries:
    target: "< 50ms for p95 of all queries"
    prohibited: "No N+1 queries, no full table scans in production"

security_requirements:
  authentication:
    requirement: "OAuth 2.0 + PKCE for web, JWT for API"
    mfa: "Required for all admin users, optional for end users"
    session_timeout: "30 minutes idle, 8 hours absolute"

  data_encryption:
    at_rest: "AES-256, keys managed in AWS KMS"
    in_transit: "TLS 1.3 minimum, no downgrade to 1.2"
    prohibited: "NEVER log or cache decrypted sensitive data"

scalability_requirements:
  current_load:
    users: "50K daily active users"
    requests: "2M API requests/day"
    data: "5TB database, growing 500GB/month"

  target_load_12_months:
    users: "200K daily active users (4x)"
    requests: "10M API requests/day (5x)"
    data: "11TB database"

  architecture_implication:
    - "Horizontal scaling must be possible (stateless services)"
    - "Database read replicas for read-heavy operations"
    - "Caching layer (Redis) for frequently accessed data"
    - "CDN for static assets"
```

---

### Anti-Pattern 4: Missing Context

❌ **Bad**:
```yaml
constraints:
  - "Must use AWS"
  - "No PHP"
  - "Require code review"
```

✅ **Good**:
```yaml
constraints:
  cloud_provider:
    requirement: "Must use AWS"
    rationale: "Existing infrastructure, team expertise, enterprise agreement
      with 40% discount"
    prohibited: "No GCP or Azure for production (OK for experimentation)"
    exception_process: "CTO approval required for other clouds, with business case"

  programming_languages:
    prohibited: "No new PHP code"
    rationale: "Legacy monolith is PHP - in migration. Team PHP expertise
      retiring in 2025. Recruiting PHP developers is difficult."
    existing_php: "Maintain only - no new features"
    approved_languages:
      backend: "Node.js (TypeScript), Python, Go"
      frontend: "TypeScript (React), no plain JavaScript"
      rationale: "Type safety reduces bugs, team consensus"

  development_process:
    code_review:
      requirement: "All code requires 2 approvals before merge"
      rationale: "Reduced production bugs 75% since implementing in 2023"
      who_can_approve: "Senior engineers and above (currently 8 people)"
      review_sla: "First review within 4 business hours, second within 24 hours"
      exception: "Hotfixes can merge with 1 approval + post-merge review"
```

---

## Section-Specific Tips

### Executive Summary

✅ **Do**:
- Include quantitative metrics
- Be specific about differentiation
- State current position honestly
- Include 3-5 year vision

❌ **Don't**:
- Use marketing buzzwords
- Be vague about metrics
- Overstate capabilities
- Make it too long (should fit on one "page")

---

### Technology Landscape

✅ **Do**:
- Include versions of key technologies
- Explain technology choices
- Be honest about technical debt
- Note what's legacy vs modern
- Include integration complexity

❌ **Don't**:
- Hide technical debt
- Be vague ("modern stack")
- Forget to mention constraints
- Miss critical dependencies

---

### Constraints and Requirements

✅ **Do**:
- Be extremely specific
- Explain implications
- Include consequences of violations
- Note prohibited approaches
- Reference specific regulations

❌ **Don't**:
- Be vague ("need good security")
- Miss regulatory requirements
- Forget organizational constraints
- Skip budget/timeline realities

---

## Real Examples

### Example 1: Technology Standard with Context

```yaml
api_design_standard:
  standard: "RESTful APIs using OpenAPI 3.0 specification"

  rationale:
    - "Team familiarity - all 12 backend engineers know REST"
    - "Tooling maturity - excellent code generation from OpenAPI specs"
    - "Client compatibility - all our customers can consume REST"

  required_practices:
    versioning: "URL-based versioning (/v1/, /v2/) not header-based"
    versioning_rationale: "Easier debugging, clear in logs, simpler CDN caching"

    authentication: "Bearer token (JWT) in Authorization header"
    error_format: "RFC 7807 Problem Details for consistent error responses"

    pagination: "Cursor-based for lists (not offset-based)"
    pagination_rationale: "Prevents issues when data changes during pagination"

  prohibited:
    - "No SOAP (legacy integration only, no new APIs)"
    - "No GraphQL for external APIs (internal experimentation OK)"
    - "No custom binary protocols (maintenance burden)"

  exceptions:
    graphql_internal: "GraphQL OK for internal admin tools (not customer-facing)"
    websockets: "WebSockets approved for real-time features (e.g., chat)"
    grpc: "Under evaluation for microservice-to-microservice communication"

  example_api:
    url: "https://api.example.com/v1/customers"
    openapi_spec: "docs/openapi/customers-v1.yaml"
    generated_clients: "JavaScript, Python, Java (auto-generated from spec)"
```

---

### Example 2: Customer Segment with Decision Context

```yaml
customer_segment:
  name: "Healthcare Provider - Mid-Size Clinics"

  profile:
    organization_size: "2-10 clinic locations, 50-200 total staff"
    geography: "United States only (HIPAA compliance complexity)"
    annual_revenue: "$5M-$50M"
    tech_sophistication: "Low to medium - often outsource IT"

  decision_making:
    primary_decision_maker: "Practice Administrator or Office Manager"
    technical_influencer: "Outsourced IT consultant (often recommends against complex systems)"
    financial_authority: "Practice Owner/Partners"

    decision_process:
      duration: "3-6 months (slow, careful)"
      steps:
        - stage: "Awareness"
          duration: "1-2 months"
          activities: "Research, peer recommendations, conference attendance"
        - stage: "Evaluation"
          duration: "1-2 months"
          activities: "Demos, trial, reference calls, security review"
        - stage: "Approval"
          duration: "1-2 months"
          activities: "Partner meetings, budget approval, legal review"

    decision_criteria:
      must_haves:
        - "HIPAA compliance (fully documented and certified)"
        - "Integrates with their specific EHR system (top 3: Epic, Cerner, Allscripts)"
        - "Works on iPads (staff workflow requirement)"
        - "Phone support during business hours (not just email)"
        - "Proven track record in healthcare (3+ similar customers)"

      nice_to_haves:
        - "Mobile app for doctors"
        - "Reporting and analytics"
        - "Integration with billing system"

      deal_breakers:
        - "Requires on-premise servers (no IT staff)"
        - "Complex setup (>2 weeks)"
        - "Annual contract >$50K (budget constraints)"
        - "Requires dedicated IT person"

  pain_points:
    primary:
      problem: "Paper-based patient intake forms"
      impact: "15 minutes per patient processing forms, 200 patients/week = 50 hours/week staff time"
      cost: "$30K/year in staff time + storage costs + errors"
      current_solution: "Manual data entry from paper to EHR"
      why_not_solved: "Tried digital forms before - too complicated, staff resisted"

  buying_behavior:
    budget: "$10K-$30K/year typical"
    payment_preference: "Monthly subscription (not annual upfront)"
    contract_length: "Prefer month-to-month or quarterly (risk averse)"
    approval_process: "Demo → Trial → Partner meeting → Legal review → Purchase"

  success_metrics:
    time_to_value: "Must see value within 2 weeks (low patience for long rollout)"
    adoption_target: "80%+ staff adoption within 1 month"
    roi_expectation: "Positive ROI within 6 months"

  our_positioning:
    - "Healthcare-specific solution (not adapted from other industries)"
    - "Simple setup - up and running in 2 days"
    - "iPad-first design (matches their workflow)"
    - "HIPAA compliant with full documentation"
    - "Integrates with top 3 EHR systems"
    - "Affordable - $499/month/location"
```

---

[← Back to Usage Guide](usage-guide.md) | [Maintenance Guide →](maintenance-guide.md)
