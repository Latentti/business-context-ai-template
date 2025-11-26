# Good Examples for Business Context Documents

Examples of high-quality, AI-useful content for each major section.

## Executive Summary - Good Example

```yaml
executive_summary:
  company_name: "NordicPay Solutions Oy"
  tagline: "B2B payment orchestration for Nordic e-commerce"

  founded:
    year: 2018
    incorporated_year: 2018

  ownership_structure: "Private, VC-backed (Series B, 2023)"

  market_position: |
    #2 payment orchestrator in Finland by transaction volume.
    Market share: 23% (vs Checkout Finland 45%, others <15%).
    Differentiation: Multi-PSP routing, 40% lower fees for high-volume merchants.

  key_metrics:
    annual_revenue: "€8.2M (2024 projected, +34% YoY)"
    arr: "€7.8M"
    employees: 67
    customers: 340 (280 SMB, 52 mid-market, 8 enterprise)
    transactions_per_year: "48M transactions, €2.1B GMV"
    average_deal_size: "SMB: €180/mo, Mid-market: €2,400/mo, Enterprise: €12,000/mo"

  competitive_advantage:
    core_differentiator: |
      Intelligent payment routing across 12 PSPs reduces transaction fees
      by average 0.3% for merchants processing >€1M/year.
      No competitor offers real-time routing optimization in Nordics.
    key_strengths:
      - "Payment routing engine: 12 PSP integrations, real-time fee optimization"
      - "Nordic specialization: Native support for MobilePay, Swish, Vipps, Finnish banks"
      - "Technical reliability: 99.98% uptime, P99 latency 89ms"

  vision_3_5_years: |
    Become #1 payment orchestrator in Nordics by 2027.
    Target: 35% market share Finland, expand to Sweden (2025) and Norway (2026).
    Revenue target: €25M ARR by 2027.

  mission_statement: "Make cross-border Nordic payments as simple as domestic ones"
```

**Why This Is Good:**
- Specific numbers everywhere
- Market position with actual percentages
- Competitive advantage is concrete and measurable
- Vision has timeline and measurable targets

---

## Technology Landscape - Good Example

```yaml
technology_landscape:
  technology_strategy:
    strategic_direction: "Cloud-native, API-first, event-driven architecture"
    technology_principles:
      - "Build vs Buy: Build core payment logic, buy commodity (auth, monitoring)"
      - "Cloud: AWS-only, no on-prem, eu-north-1 primary"
      - "Languages: TypeScript for services, Python for data/ML, Go for performance-critical"

  application_portfolio:
    core_business_systems:
      - system_name: "Payment Gateway"
        category: "Core Platform"
        vendor_or_custom: "Custom built"
        technology: "Node.js 20, TypeScript, PostgreSQL 15"
        business_functions: "Payment processing, PSP routing, transaction management"
        users: "All merchants via API"
        integration_criticality: "Critical"
        technical_health: "Modern"
        notes: "Rebuilt in 2023, handles 1,500 TPS peak"

      - system_name: "Merchant Portal"
        category: "Customer-facing"
        vendor_or_custom: "Custom built"
        technology: "Next.js 14, React 18, TypeScript"
        business_functions: "Merchant onboarding, dashboard, reporting"
        users: "340 merchant accounts, ~800 users"
        technical_health: "Modern"

      - system_name: "Salesforce"
        category: "CRM"
        vendor_or_custom: "Salesforce Sales Cloud"
        version: "Enterprise Edition"
        business_functions: "Sales pipeline, customer management"
        users: "Sales team (12 users)"
        integration_criticality: "Medium"
        integrations: "Bidirectional sync with Merchant Portal"
        technical_health: "Adequate"
        notes: "Considering migration to HubSpot for cost (€45K/year vs €18K)"

  technical_architecture:
    architecture_style: "Event-driven microservices"

    infrastructure:
      hosting_model: "Cloud (AWS)"
      cloud_providers:
        - provider: "AWS"
          region: "eu-north-1 (Stockholm)"
          services: [EKS, RDS, ElastiCache, SQS, Lambda, S3, CloudFront]
          monthly_spend: "€32-38K"
          cost_trend: "Stable, optimized in Q2 2024"

      deployment:
        orchestration: "Kubernetes (EKS 1.29)"
        cluster_size: "Production: 18 nodes (m6i.xlarge), Staging: 6 nodes"
        deployment_method: "GitOps via ArgoCD"
        ci_cd: "GitHub Actions"
        deployments_per_week: 12-15

    services_inventory:
      - service: "payment-gateway"
        language: "TypeScript/Node.js"
        pods: 8
        critical: true
      - service: "routing-engine"
        language: "Go"
        pods: 4
        critical: true
      - service: "merchant-api"
        language: "TypeScript/Node.js"
        pods: 4
        critical: true
      - service: "notification-service"
        language: "TypeScript/Node.js"
        pods: 2
        critical: false
      - service: "reporting-service"
        language: "Python"
        pods: 2
        critical: false
      - service: "fraud-detection"
        language: "Python"
        pods: 2
        critical: true
        notes: "ML-based, retrained weekly"

  technical_debt_and_challenges:
    technical_debt_areas:
      - area: "Legacy reconciliation batch jobs"
        description: "Daily batch jobs in Python 3.8, no tests, brittle"
        impact: "2-3 hours manual fixing per week when failures occur"
        remediation_priority: "High"
        plan: "Rewrite as event-driven service, Q1 2025"

      - area: "Inconsistent API versioning"
        description: "Mix of v1, v2 APIs, some unversioned"
        impact: "Merchant confusion, support overhead"
        remediation_priority: "Medium"
        plan: "Standardize on OpenAPI 3.1, deprecation policy, Q2 2025"

    technology_constraints:
      - constraint: "PCI-DSS compliance"
        implication: "Card data only in certified systems, annual audit €50K"
      - constraint: "GDPR data residency"
        implication: "All PII must stay in EU, affects vendor selection"
      - constraint: "Bank integration latency"
        implication: "Finnish bank APIs have 2-5s response times, affects UX"
```

**Why This Is Good:**
- Specific versions and configurations
- Honest about technical debt
- Clear constraints with implications
- Costs included where relevant

---

## Constraints and Requirements - Good Example

```yaml
constraints_and_requirements:
  regulatory_and_compliance:
    regulations:
      - regulation: "PCI-DSS Level 1"
        applicability: "All systems handling card data"
        requirements:
          - "Annual QSA audit (last: Oct 2024, passed)"
          - "Quarterly vulnerability scans"
          - "Card data encryption (AES-256)"
          - "Network segmentation for cardholder data environment"
        implications: "New features touching card data require security review, adds 2-3 weeks to timeline"
        compliance_cost: "€50K/year (audit + tools)"

      - regulation: "PSD2 / SCA"
        applicability: "All payment transactions in EEA"
        requirements:
          - "Strong Customer Authentication for transactions >€30"
          - "Dynamic linking (amount + payee in auth)"
          - "Exemption handling (TRA, whitelisting, low value)"
        implications: "Must integrate with bank 3DS2 flows, affects checkout UX"

      - regulation: "GDPR"
        applicability: "All personal data processing"
        requirements:
          - "Data residency: EU only"
          - "Right to deletion: Must be implementable within 30 days"
          - "Data portability: Export in machine-readable format"
          - "Breach notification: 72h to DPA"
        implications: "Affects vendor selection, data architecture, retention policies"
        dpo_contact: "dpo@nordicpay.fi"

  security_requirements:
    security_classification: "High (financial data)"

    mandatory_controls:
      - control: "Authentication"
        requirement: "MFA required for all internal systems"
        implementation: "Okta SSO + hardware keys for production access"

      - control: "Encryption"
        requirement: "All data encrypted at rest and in transit"
        implementation: "TLS 1.3, AES-256 for stored data, AWS KMS for key management"

      - control: "Access control"
        requirement: "Principle of least privilege, quarterly access reviews"
        implementation: "Role-based access in AWS IAM, JIT access for production"

      - control: "Audit logging"
        requirement: "All access to customer data logged"
        implementation: "CloudTrail + custom audit logs, 7-year retention"

  performance_requirements:
    - requirement_type: "Response time"
      specification: "P99 < 200ms for payment API"
      current_performance: "P99 = 89ms"
      criticality: "Must-have (merchant SLAs)"

    - requirement_type: "Throughput"
      specification: "Handle 2,000 TPS sustained, 5,000 TPS peak"
      current_performance: "Tested to 3,500 TPS"
      criticality: "Must-have (Black Friday requirement)"

    - requirement_type: "Availability"
      specification: "99.95% uptime (4.38h downtime/year max)"
      current_performance: "99.98% (2024 YTD)"
      criticality: "Must-have (enterprise SLAs)"

  budget_constraints:
    project_budgets:
      small_project: "< €50K, team lead approval"
      medium_project: "€50-200K, CTO approval"
      large_project: "> €200K, board approval"

    technology_budget:
      annual_infra: "€450K (AWS, tools, SaaS)"
      annual_licenses: "€180K (Salesforce, Datadog, etc.)"
      contractor_budget: "€200K/year available"

    constraints:
      - "No new SaaS > €30K/year without CTO approval"
      - "Prefer open source for non-critical tooling"
      - "AWS commitment discount: Must stay above €25K/month"
```

**Why This Is Good:**
- Specific regulations with actual requirements
- Clear implications for development
- Performance requirements are measurable
- Budget constraints are explicit

---

## Quick Reference: What Makes Content AI-Useful

| Section | Must Include | Avoid |
|---------|--------------|-------|
| Executive Summary | Revenue, employees, customer count, market share | Taglines, vague positioning |
| Technology | Versions, deployment details, costs | Just listing technology names |
| Constraints | Specific numbers, compliance details | "Must be secure", "must be fast" |
| Capabilities | Honest maturity levels, gaps | All 5s, no gaps mentioned |
| Strategy | Timeline, measurable targets | Vague aspirations |
| Metrics | Current values, targets, trends | Metrics without numbers |
