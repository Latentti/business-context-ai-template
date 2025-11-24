# Templates

This directory contains the core business context templates in different complexity levels.

## Available Templates

### 1. business-context-quickstart.yaml
**Quick Start Template** - Minimum viable business context

- **Time to complete**: 4-6 hours
- **Sections**: 10 essential sections
- **Best for**: Startups, small teams, fast iteration
- **Coverage**: Covers the absolute minimum AI needs to understand your business

**Use when**:
- You want to get started quickly
- You're a startup or small company (< 50 people)
- You have simple organizational structure
- You need immediate value and can expand later

---

### 2. business-context-full.yaml
**Full Template** - Comprehensive TOGAF-based business architecture

- **Time to complete**: 8-16 hours
- **Sections**: 22 comprehensive sections
- **Best for**: Scale-ups, mid-size companies, multiple products
- **Coverage**: Complete TOGAF Phase B Business Architecture

**Use when**:
- You want comprehensive coverage
- You have multiple products or business units
- Your organization is moderately complex (50-500 people)
- You run multiple concurrent AI projects
- You want TOGAF-compliant business architecture

---

### 3. business-context-enterprise.yaml
**Enterprise Template** - Extended for complex organizations

- **Time to complete**: 16-40 hours
- **Sections**: Extended with enterprise-specific sections
- **Best for**: Large enterprises, complex structures, heavy regulation
- **Coverage**: Everything from Full Template plus enterprise governance

**Use when**:
- You're a large organization (500+ people)
- You have multiple business units
- Complex product portfolios
- Heavy regulatory requirements
- Need rigorous governance
- Enterprise architecture mandate

---

## How to Use

### 1. Choose Your Template

Select based on your organization size and complexity:

```bash
# Small/Startup (< 50 people)
cp business-context-quickstart.yaml ../my-company-context.yaml

# Mid-size (50-500 people)
cp business-context-full.yaml ../my-company-context.yaml

# Enterprise (500+ people)
cp business-context-enterprise.yaml ../my-company-context.yaml
```

### 2. Fill Out Your Copy

```bash
# Edit your copy (not the original template!)
vi ../my-company-context.yaml
```

**Important**: Don't edit the template files directly - always copy first!

### 3. Version Control

```bash
# Add to git (outside this template repository)
cd /your/project
git add my-company-context.yaml
git commit -m "Add business context v1.0"
git tag business-context-v1.0
```

---

## Template Comparison

| Feature | Quick Start | Full | Enterprise |
|---------|------------|------|------------|
| **Time to Complete** | 4-6 hours | 8-16 hours | 16-40 hours |
| **Sections** | 10 | 22 | 25+ |
| **Complexity** | Simple | Moderate | Complex |
| **TOGAF Compliance** | Partial | Full | Extended |
| **Best For** | Startups | Scale-ups | Enterprises |
| **Team Size** | < 50 | 50-500 | 500+ |
| **Products** | Single | Multiple | Portfolio |
| **Governance** | Basic | Standard | Rigorous |

---

## Customization

All templates can be customized:

### Add Sections
Add industry-specific or organization-specific sections:

```yaml
# Add your custom section
custom_section:
  your_field: "your value"
```

### Remove Sections
Remove sections that don't apply:

```yaml
# Just delete the section or mark as N/A
section_name: "N/A - Not applicable to our business"
```

### Reorganize
Rearrange sections to match your preferences:

```yaml
# Templates are flexible - organize as makes sense for you
```

---

## Template Structure

All templates follow this general structure:

```yaml
---
metadata:
  # Document metadata

---
## SECTION NAME
section_data:
  # Section content

---
## NEXT SECTION
...
```

### Why YAML?

- **Structured**: Easy for AI to parse
- **Readable**: Humans can read and edit
- **Flexible**: Easy to extend
- **Standard**: Widely supported

### Alternative Formats

You can convert to other formats if needed:

**Markdown**: For better readability
```bash
# Convert YAML to Markdown (use your preferred tool)
```

**JSON**: For programmatic access
```bash
# Convert YAML to JSON
python -c "import yaml, json, sys; print(json.dumps(yaml.safe_load(sys.stdin)))" < my-context.yaml > my-context.json
```

**Notion/Confluence**: For collaborative editing
- Fill out template locally
- Copy sections to Notion/Confluence
- Export back to YAML for AI use

---

## Validation

Before using your filled template, validate it:

### Basic Validation

```bash
# Check YAML syntax
python -c "import yaml; yaml.safe_load(open('my-company-context.yaml'))"
```

### Content Validation

Use the validation checklist: `../tools/validation-checklist.md`

- [ ] All required sections filled
- [ ] No placeholder text remaining
- [ ] Specific, not generic descriptions
- [ ] Numbers and metrics included
- [ ] Constraints clearly stated
- [ ] Validated by stakeholders

---

## Examples

See filled example templates in the `../examples/` directory:

- **Tech Startup**: `../examples/tech-startup-example.yaml`
- **Enterprise**: `../examples/enterprise-example.yaml`
- **E-commerce**: `../examples/ecommerce-example.yaml`

These show real-world examples of completed templates.

---

## Support

Need help choosing or filling out a template?

- **Documentation**: See `../docs/usage-guide.md`
- **Best Practices**: See `../docs/best-practices.md`
- **FAQ**: See `../docs/faq.md`
- **Issues**: [GitHub Issues](https://github.com/Latentti/business-context-ai-template/issues)

---

## Contributing

Found a way to improve the templates?

See `../CONTRIBUTING.md` for guidelines on:
- Suggesting template improvements
- Adding new sections
- Submitting changes

---

**Ready to start?** Choose your template and begin filling it out!

[← Back to Main README](../README.md)
