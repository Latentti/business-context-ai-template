# Business Context AI Template

> **The "AI Pitch" for Your Business** - A comprehensive, TOGAF-based template for providing business context to AI development tools.

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![TOGAF](https://img.shields.io/badge/TOGAF-Phase%20B-blue.svg)](https://www.opengroup.org/togaf)
[![Version](https://img.shields.io/badge/version-1.0.0-green.svg)](https://github.com/Latentti/business-context-ai-template)

---

## 🎯 What Is This?

When using AI-driven development tools (like Claude, GitHub Copilot, BMad, or similar), you typically spend significant time explaining your business context in every project:

- Who you are as a company
- What products/services you offer
- Your technology stack and constraints
- Your strategic objectives
- Regulatory requirements you must follow

**This template solves that problem.**

Create your business context **once**, reference it in **every AI project**, and save hours of repetitive briefing.

---

## 💡 The Problem This Solves

### Without Business Context Template

```
You → AI: "Build a payment feature for our mobile app"

AI: "Sure! Should I use Stripe or PayPal? What currencies?
What are your security requirements? What data can I access?
What's your tech stack? How do you handle errors?
What's your testing strategy? [+100 more questions...]"

You: [Spends 2-4 hours answering questions]
```

### With Business Context Template

```
You → AI: "Load Business_Context.yaml. Build a payment feature
for the B2C segment (Section 6.3) in our mobile app."

AI: "Understood from your business context:
- I'll integrate with your Paytrail payment provider (Section 10)
- Support EUR and SEK per your markets (Section 6)
- Implement PSD2 SCA compliance (Section 15)
- Follow your mobile-first design principles (Section 15)
- Use your standard tech stack: React Native + Node.js (Section 10)
- Include GDPR-compliant data handling (Section 15)

For this specific feature, tell me:
1. One-time payment, recurring, or both?
2. Any project-specific requirements?"

You: [Answers 2-3 project-specific questions]
```

**Result:** 100 questions → 3 questions. Hours → Minutes.

---

## 🚀 Quick Start

### 1. Choose Your Template

We provide **three templates** for different needs:

- **📋 Quick Start** (4-6 hours) - Minimum viable business context with 10 essential sections
- **📚 Full Template** (8-16 hours) - Comprehensive TOGAF-based template with 22 sections
- **🏢 Enterprise** (16-40 hours) - Extended template for complex organizations

### 2. Copy and Fill

```bash
# Clone this repository
git clone https://github.com/Latentti/business-context-ai-template.git

# Choose your template
cd business-context-ai-template/templates

# Copy the template that fits your needs
cp business-context-quickstart.yaml ../my-company-context.yaml

# Fill it out (see docs/usage-guide.md for help)
```

### 3. Use in AI Projects

```
# In your AI development tool:
"Load [path]/my-company-context.yaml for complete business understanding
before we start the project."
```

---

## 📖 Documentation

### Core Documents

- **[Usage Guide](docs/usage-guide.md)** - Step-by-step guide to filling out the template
- **[Best Practices](docs/best-practices.md)** - How to write effective business context for AI
- **[Maintenance Guide](docs/maintenance-guide.md)** - Keeping your context up to date
- **[FAQ](docs/faq.md)** - Common questions and answers

### Templates

- **[Quick Start Template](templates/business-context-quickstart.yaml)** - 10 essential sections (4-6h)
- **[Full Template](templates/business-context-full.yaml)** - 22 comprehensive sections (8-16h)
- **[Enterprise Template](templates/business-context-enterprise.yaml)** - Extended for complex orgs (16-40h)

### Examples

- **[Tech Startup Example](examples/tech-startup-example.yaml)** - SaaS company example
- **[Enterprise Example](examples/enterprise-example.yaml)** - Large organization example
- **[E-commerce Example](examples/ecommerce-example.yaml)** - Online retail example

---

## 🏗️ Template Structure

Our templates are based on **TOGAF Phase B (Business Architecture)** framework to ensure comprehensive coverage:

### Core Sections

1. **Executive Summary** - Quick business overview
2. **Company Profile** - Organizational details
3. **Business History** - Context and evolution
4. **Core Business & Value Proposition** - What you do and why customers choose you
5. **Products and Services** - What you sell
6. **Customer Segments** - Who you serve
7. **Competitive Landscape** - Market position and differentiation
8. **Business Capabilities** - What your business can do (TOGAF capability model)
9. **Business Processes & Value Streams** - How work flows
10. **Technology Landscape** - Current tech environment
11. **Data and Analytics** - Data assets and capabilities
12. **Operating Model** - How your organization works
13. **Strategic Objectives** - Where you're going
14. **Success Metrics** - How you measure success
15. **Constraints & Requirements** - Boundaries AI must respect
16. **Stakeholders** - Who's involved
17. **Partnerships** - Your ecosystem
18. **Risks & Challenges** - What to watch out for
19. **Culture & Dynamics** - Organizational culture
20. **AI Development Context** - How you work with AI
21. **Lessons Learned** - Past learnings and preferences
22. **Future Vision** - Long-term aspirations

---

## ✨ Key Features

### 📊 TOGAF-Based Structure
Built on enterprise architecture best practices (TOGAF Phase B - Business Architecture)

### 🤖 AI-Optimized
Designed specifically for AI consumption - structured, comprehensive, context-rich

### 🔧 Three Complexity Levels
Choose the template that fits: Quick Start (4-6h), Full (8-16h), or Enterprise (16-40h)

### 📚 Comprehensive Documentation
Step-by-step guides, examples, and best practices included

### 🎯 Industry Agnostic
Works for startups, scale-ups, enterprises, any industry

### 🔄 Maintainable
Includes version control, update triggers, and maintenance schedules

### 🌍 Multi-Language Ready
Templates can be filled in any language

---

## 📊 Benefits

### Measurable Benefits

- ⏱️ **Project Start Speed**: 2-4 hours → 15-30 minutes
- 🎯 **Fewer Questions**: 100+ questions → ~10 questions
- 🔄 **Consistency**: Same understanding across all projects
- 📈 **Quality**: Better strategic alignment
- 💰 **Cost Efficiency**: Less rework and iterations

### Qualitative Benefits

- ✨ Better AI understanding of your business
- 🚀 Faster onboarding (new team members, consultants, AI tools)
- 🎓 Organizational learning captured
- 🔐 Knowledge preservation (not just in people's heads)
- 🤝 Better collaboration across teams

---

## 🎓 Who Is This For?

### Perfect For:

- **Product Managers** - Briefing AI tools for product development
- **CTOs/Tech Leads** - Establishing technical context for AI development
- **Business Analysts** - Documenting business requirements for AI
- **Enterprise Architects** - Creating comprehensive business architecture
- **Startup Founders** - Quickly establishing business context for AI tools
- **Development Teams** - Using AI-assisted development (GitHub Copilot, Claude, etc.)

### Use Cases:

- AI-driven software development (BMad, Claude Code, GitHub Copilot)
- Onboarding new developers or consultants
- Vendor briefings and RFPs
- Strategic planning sessions
- Architecture documentation
- Any situation requiring comprehensive business understanding

---

## 🛠️ Tools Included

### [Checklist Tool](tools/completion-checklist.md)
Track your progress filling out the template

### [Validation Tool](tools/validation-checklist.md)
Ensure your context is complete and AI-ready

### [Update Template](tools/update-template.md)
Structured approach to updating your context

### [Section Priority Guide](tools/section-priority-guide.md)
Which sections to fill first based on your needs

---

## 🤝 Contributing

We welcome contributions! Whether it's:

- 🐛 Bug reports
- 💡 Feature suggestions
- 📝 Documentation improvements
- 🌍 Translations
- 📚 Additional examples

See [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines.

---

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

You are free to:
- ✅ Use commercially
- ✅ Modify
- ✅ Distribute
- ✅ Private use

---

## 🌟 Examples in the Wild

Organizations using this template (with permission):

> 📢 **Want to be featured?** Submit a PR adding your organization!

---

## 📚 Additional Resources

### Related Frameworks
- [TOGAF (The Open Group Architecture Framework)](https://www.opengroup.org/togaf)
- [Business Architecture Guild](https://www.businessarchitectureguild.org/)
- [Zachman Framework](https://www.zachman.com/)

### AI Development Tools
- [Claude (Anthropic)](https://www.anthropic.com/claude)
- [GitHub Copilot](https://github.com/features/copilot)
- [BMad Methodology](https://github.com/Latentti/bmad-methodology) _(AI-driven development methodology)_

### Business Architecture
- [TOGAF Standard](https://pubs.opengroup.org/togaf-standard/)
- [Business Capability Modeling](https://www.businessarchitectureguild.org/page/Capabilities)

---

## 📮 Contact & Support

- **Issues**: [GitHub Issues](https://github.com/Latentti/business-context-ai-template/issues)
- **Discussions**: [GitHub Discussions](https://github.com/Latentti/business-context-ai-template/discussions)
- **Email**: ari.hietamaki@latentti.fi
- **Creator**: Ari Hietamäki, Latentti Oy

---

## 🗺️ Roadmap

### Version 1.0 (Current)
- ✅ Core templates (Quick Start, Full, Enterprise)
- ✅ Comprehensive documentation
- ✅ Three industry examples
- ✅ Basic tools (checklists, validators)

### Version 1.1 (Planned)
- [ ] Interactive web-based template builder
- [ ] Additional industry-specific examples
- [ ] Template validation tool (automated)
- [ ] Multi-language documentation

### Version 2.0 (Future)
- [ ] AI-assisted template filling
- [ ] Integration templates for popular AI tools
- [ ] Template analytics and insights
- [ ] Community template library

---

## 📈 Project Stats

- **Templates**: 3 (Quick Start, Full, Enterprise)
- **Examples**: 3 (Tech Startup, Enterprise, E-commerce)
- **Documentation Pages**: 15+
- **Supported Languages**: Any (template is language-agnostic)
- **Lines of Documentation**: 5000+

---

## 🙏 Acknowledgments

Built with inspiration from:
- **TOGAF** - The Open Group Architecture Framework
- **Business Architecture Guild** - Business capability modeling
- **Enterprise Architecture** - Best practices from EA community
- **AI Development Community** - Feedback from practitioners using AI tools

---

## 📜 Changelog

### [1.0.0] - 2025-11-24

#### Added
- Initial release
- Quick Start template (10 sections)
- Full template (22 sections)
- Enterprise template (extended)
- Comprehensive documentation
- Three industry examples
- Tool suite (checklists, validators)

See [CHANGELOG.md](CHANGELOG.md) for full version history.

---

## 🚀 Get Started Now

```bash
# 1. Clone the repository
git clone https://github.com/Latentti/business-context-ai-template.git

# 2. Choose your template
cd business-context-ai-template/templates

# 3. Copy and start filling
cp business-context-quickstart.yaml ../my-company-context.yaml

# 4. Read the usage guide
open ../docs/usage-guide.md

# 5. Start using in your AI projects!
```

---

<div align="center">

**[⬆ Back to Top](#business-context-ai-template)**

Made with ❤️ by Ari Hietamäki & Latentti Oy for the AI development community

**Star ⭐ this repo if you find it useful!**

</div>
