# Anti-Patterns in Business Context Documents

Common mistakes that reduce the usefulness of business context for AI development.

## Category 1: Marketing Language

### Pattern: Superlatives Without Evidence
**Red Flag Words:** best, leading, top, premier, world-class, industry-leading, cutting-edge, innovative, revolutionary

**Examples:**
| ❌ Bad | ✅ Good |
|--------|---------|
| "We are the leading provider of..." | "Market share: 34% in Finland (source: Gartner 2024), #1 by customer count" |
| "Our world-class customer service..." | "NPS: 72 (industry avg: 45), avg response time: 4h, resolution rate: 94%" |
| "Cutting-edge technology stack" | "AWS-native, Kubernetes 1.28, PostgreSQL 15, migrated from legacy in 2023" |
| "Best-in-class performance" | "P99 latency: 145ms, 99.94% uptime (2024 YTD), 2M tx/day capacity" |

**Why It's Bad:** AI cannot make technical decisions based on adjectives. It needs specific metrics, comparisons, and evidence.

---

### Pattern: Vague Quantities
**Red Flag Words:** many, several, few, some, significant, substantial, numerous, various

**Examples:**
| ❌ Bad | ✅ Good |
|--------|---------|
| "We have many enterprise customers" | "127 enterprise customers (>1000 employees), 68% of ARR" |
| "Several integrations available" | "47 pre-built integrations: 12 ERP, 15 CRM, 20 payment gateways" |
| "Significant market presence" | "Operations in 12 countries, 45% revenue from Nordics, 30% DACH" |
| "Various technology capabilities" | "Core competencies: React (8 devs), Python/ML (5), AWS (12 certified)" |

**Why It's Bad:** "Many" could mean 5 or 5000. AI needs actual numbers to understand scale.

---

### Pattern: Buzzword Bingo
**Red Flag Words:** synergy, leverage, optimize, holistic, seamless, robust, scalable, agile, dynamic

**Examples:**
| ❌ Bad | ✅ Good |
|--------|---------|
| "We leverage AI to optimize operations" | "ML-based demand forecasting reduces overstock by 23%, saves €1.2M/year" |
| "Seamless integration capabilities" | "REST API, webhook support, avg integration time: 2-4 weeks" |
| "Robust and scalable platform" | "Handles 50K concurrent users, auto-scales to 200K, tested to 500K" |
| "Agile development methodology" | "2-week sprints, CI/CD via GitHub Actions, 15 deployments/week avg" |

**Why It's Bad:** Buzzwords hide the actual capabilities. AI needs concrete details.

---

## Category 2: Vague Claims

### Pattern: Opinion Stated as Fact
**Red Flag Phrases:** "we believe", "we think", "we feel", "is considered", "is known for", "is recognized as"

**Examples:**
| ❌ Bad | ✅ Good |
|--------|---------|
| "We believe our platform is superior" | "Platform comparison: 40% faster processing, 25% lower TCO vs Competitor X (internal benchmark 2024)" |
| "We are known for reliability" | "99.97% uptime (2024), 0 major incidents in 18 months, SOC 2 Type II certified" |
| "Our team is considered highly skilled" | "Avg 8 years experience, 12 AWS certified, 6 with advanced CS degrees" |

**Why It's Bad:** AI needs verifiable facts, not opinions.

---

### Pattern: Future Promises as Current State
**Red Flag Phrases:** "will be", "planning to", "working on", "soon", "in the future", "roadmap includes"

**Examples:**
| ❌ Bad | ✅ Good |
|--------|---------|
| "We will be launching AI features" | "Current: Rule-based automation. Q2 2025: ML recommendations (beta). 2026: Full AI suite" |
| "Planning to expand to new markets" | "Current: Finland, Sweden. 2025: Norway, Denmark (LOI signed). 2026+: DACH (exploratory)" |
| "Working on mobile app" | "Mobile app: Development started Oct 2024, MVP target Mar 2025, public launch Q3 2025" |

**Why It's Bad:** AI needs to know what exists NOW to make relevant recommendations. Future state should be clearly marked as such.

---

## Category 3: Missing Critical Information

### Pattern: Technology Without Context
**Example:**
```yaml
# ❌ Bad
technology_stack:
  - AWS
  - Kubernetes
  - PostgreSQL
  - React

# ✅ Good
technology_stack:
  aws:
    services: [EKS, RDS, S3, Lambda, CloudFront]
    account_structure: "Multi-account (prod, staging, dev)"
    monthly_spend: "€45-55K"
    expertise_level: "Advanced (12 certified engineers)"
  kubernetes:
    version: "1.28"
    cluster_size: "Production: 24 nodes, Staging: 8 nodes"
    managed_by: "EKS"
    deployment: "Helm charts, ArgoCD"
```

**Why It's Bad:** Listing technology names doesn't tell AI how it's used, at what scale, or what constraints exist.

---

### Pattern: Constraints Without Specifics
**Example:**
```yaml
# ❌ Bad
requirements:
  security: "Must be secure"
  performance: "Must be fast"
  compliance: "GDPR compliant"

# ✅ Good
requirements:
  security:
    authentication: "SAML 2.0 SSO required, MFA mandatory"
    data_encryption: "AES-256 at rest, TLS 1.3 in transit"
    audit: "All data access logged, 7-year retention"
    penetration_testing: "Annual third-party pentest required"
  performance:
    response_time: "P99 < 200ms for user-facing APIs"
    throughput: "Must handle 10K requests/second peak"
    availability: "99.9% uptime SLA, max 8.76h downtime/year"
  compliance:
    gdpr:
      data_residency: "EU only (currently AWS eu-north-1)"
      data_subjects: "Finnish and Swedish residents"
      dpo_contact: "dpo@company.fi"
      breach_notification: "72h to authorities, 48h to affected users"
```

**Why It's Bad:** Vague constraints don't help AI design compliant solutions.

---

## Category 4: Inconsistencies

### Pattern: Conflicting Numbers
**Example:**
```yaml
# ❌ Bad - Numbers don't add up
executive_summary:
  employees: 150

departments:
  engineering: 45
  sales: 30
  marketing: 20
  operations: 25
  # Total: 120... where are the other 30?

# ✅ Good - Numbers are consistent
executive_summary:
  employees: 150

departments:
  engineering: 45
  sales: 30
  marketing: 20
  operations: 25
  customer_success: 15
  hr_and_admin: 10
  leadership: 5
  # Total: 150 ✓
```

**Why It's Bad:** Inconsistencies make AI question all data reliability.

---

### Pattern: Technology Contradictions
**Example:**
```yaml
# ❌ Bad - Contradictory information
architecture:
  style: "Microservices"

technology:
  main_application: "Monolithic Java application (Spring Boot)"

# ✅ Good - Honest current state
architecture:
  current_style: "Hybrid - transitioning from monolith to microservices"
  monolith_percentage: "60% of functionality"
  microservices_percentage: "40% of functionality"
  migration_status: "In progress, target completion Q4 2025"

technology:
  legacy_monolith:
    stack: "Java 11, Spring Boot 2.7"
    status: "Maintained, gradually decomposing"
    timeline: "Full sunset by 2026"
  new_services:
    stack: "Java 17, Spring Boot 3, Kotlin for new services"
    count: "12 microservices in production"
```

**Why It's Bad:** AI will be confused about actual architecture and may suggest incompatible solutions.

---

## Category 5: Overselling

### Pattern: Inflated Capability Maturity
**Example:**
```yaml
# ❌ Bad - Suspiciously high ratings
capabilities:
  data_analytics:
    maturity: 5  # "Optimized"
    description: "We have dashboards"

  ai_ml:
    maturity: 4  # "Managed"
    description: "We use ChatGPT sometimes"

# ✅ Good - Honest assessment
capabilities:
  data_analytics:
    maturity: 2  # "Developing"
    description: "Basic BI dashboards in Metabase. Manual reporting. No self-service analytics yet."
    gaps: "No data warehouse, limited data quality processes"

  ai_ml:
    maturity: 1  # "Initial"
    description: "Experimental use of LLMs for internal tasks. No production ML."
    gaps: "No MLOps, no data science team, limited clean training data"
```

**Why It's Bad:** Inflated maturity leads to unrealistic AI recommendations that the organization can't execute.

---

## Quick Reference: Red Flags

| Category | Red Flags | What to Ask |
|----------|-----------|-------------|
| Marketing | best, leading, innovative, world-class | "What metric proves this?" |
| Vague Quantities | many, several, significant | "What's the exact number?" |
| Opinions | we believe, is considered, is known for | "What evidence supports this?" |
| Future State | will be, planning to, soon | "What's the specific timeline?" |
| Missing Context | Technology names without details | "What version? How used? Scale?" |
| Inconsistencies | Numbers that don't add up | "Can you reconcile these figures?" |
| Overselling | All high maturity ratings | "What gaps exist? Be honest." |
