# Business Context AI Template

> **The "AI Pitch" for Your Business** - A comprehensive, TOGAF-based template for providing business context to AI development tools.

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![TOGAF](https://img.shields.io/badge/TOGAF-Phase%20B-blue.svg)](https://www.opengroup.org/togaf)
[![Version](https://img.shields.io/badge/version-1.0.0-green.svg)](https://github.com/Latentti/business-context-ai-template)
[![Claude Code](https://img.shields.io/badge/Claude%20Code-Agent%20Included-blueviolet.svg)](https://claude.ai/claude-code)

---

## 🤖 NEW: AI-Assisted Template Filling with Claude Code

**This repository includes a built-in Claude Code agent** that guides you through filling the template interactively:

```bash
# Clone and start immediately
git clone https://github.com/Latentti/business-context-ai-template.git
cd business-context-ai-template
claude

# Start the guided workflow
/BizContext/start
```

The **Business Context Architect** agent will:
- 🎯 Guide you section by section
- ⚠️ Challenge vague or marketing-style content
- 📊 Demand specific numbers and evidence
- 🌍 Accept input in any language, write output in English
- ✅ Validate your document for AI-readiness

**Result:** What would take 8-16 hours of manual work becomes a guided 4-6 hour conversation.

[📖 See Claude Code Guide →](docs/claude-code-guide.md)

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

### Option A: AI-Guided (Recommended) ⭐

Use the built-in Claude Code agent for interactive, fact-checked filling:

```bash
# Clone and start
git clone https://github.com/Latentti/business-context-ai-template.git
cd business-context-ai-template
claude

# Start the guided workflow
/BizContext/start
```

The agent will guide you through each section, challenge vague content, and ensure quality.

### Option B: Manual Filling

Fill the template yourself using the documentation:

```bash
# Clone this repository
git clone https://github.com/Latentti/business-context-ai-template.git
cd business-context-ai-template/templates

# Copy the template that fits your needs
cp business-context-full.yaml ../my-company-context.yaml

# Fill it out (see docs/usage-guide.md for help)
```

### Template Options

| Template | Sections | Time | Best For |
|----------|----------|------|----------|
| **📋 Quick Start** | 10 | 4-6h | Startups, small teams |
| **📚 Full** | 22 | 8-16h | Scale-ups, mid-size |
| **🏢 Enterprise** | 22+ | 16-40h | Large organizations |

### Use in AI Projects

```
# In your AI development tool:
"Load [path]/my-company-context.yaml for complete business understanding
before we start the project."
```

---

## 📖 Documentation

### Core Documents

- **[Claude Code Guide](docs/claude-code-guide.md)** ⭐ - AI-assisted template filling (recommended)
- **[Usage Guide](docs/usage-guide.md)** - Manual step-by-step guide
- **[Best Practices](docs/best-practices.md)** - How to write effective business context for AI

### Templates

- **[Quick Start Template](templates/business-context-quickstart.yaml)** - 10 essential sections (4-6h)
- **[Full Template](templates/business-context-full.yaml)** - 22 comprehensive sections (8-16h)
- **[Enterprise Template](templates/business-context-enterprise.yaml)** - Extended for complex orgs (16-40h)

### Reference Data (in `.bizcontext-core/data/`)

- **[Anti-Patterns](.bizcontext-core/data/anti-patterns.md)** - Common mistakes to avoid
- **[Good Examples](.bizcontext-core/data/good-examples.md)** - Examples of quality content

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

### 🤖 AI-Assisted Filling (NEW!)
Built-in Claude Code agent guides you interactively, challenges vague content, ensures quality

### 📊 TOGAF-Based Structure
Built on enterprise architecture best practices (TOGAF Phase B - Business Architecture)

### ⚡ AI-Optimized
Designed specifically for AI consumption - structured, comprehensive, context-rich

### 🔧 Three Complexity Levels
Choose the template that fits: Quick Start (4-6h), Full (8-16h), or Enterprise (16-40h)

### 📚 Comprehensive Documentation
Step-by-step guides, examples, and best practices included

### 🎯 Industry Agnostic
Works for startups, scale-ups, enterprises, any industry

### 🔄 Maintainable
Includes version control, update triggers, and maintenance schedules

### 🌍 Multi-Language Input
Describe your business in any language - output is always English for AI compatibility

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

### 🤖 Claude Code Agent (NEW!)
Interactive AI assistant for template filling - the fastest way to create quality content.

| Command | Description |
|---------|-------------|
| `/BizContext/start` | Start guided template filling workflow |
| `/BizContext/fill-section` | Fill a specific section interactively |
| `/BizContext/critique` | Evaluate content for AI-usefulness |
| `/BizContext/validate` | Run full document validation |

[📖 Claude Code Guide →](docs/claude-code-guide.md)

### 📋 Manual Tools

- **[Checklist Tool](tools/completion-checklist.md)** - Track your progress filling out the template
- **[Validation Tool](tools/validation-checklist.md)** - Ensure your context is complete and AI-ready
- **[Update Template](tools/update-template.md)** - Structured approach to updating your context
- **[Section Priority Guide](tools/section-priority-guide.md)** - Which sections to fill first based on your needs

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
- ✅ Basic tools (checklists, validators)
- ✅ **Claude Code Agent for AI-assisted filling**
- ✅ **Fact-checking and quality validation**
- ✅ **Multi-language input support**

### Version 1.1 (Planned)
- [ ] Interactive web-based template builder
- [ ] Additional industry-specific examples
- [ ] Template validation tool (automated)
- [ ] Multi-language documentation

### Version 2.0 (Future)
- [ ] Integration templates for popular AI tools
- [ ] Template analytics and insights
- [ ] Community template library
- [ ] VS Code extension

---

## 📈 Project Stats

- **Templates**: 3 (Quick Start, Full, Enterprise)
- **Claude Code Commands**: 4 (start, fill-section, critique, validate)
- **Documentation Pages**: 20+
- **Input Languages**: Any (output always English)
- **Lines of Code/Documentation**: 10,000+

---

## 🙏 Acknowledgments

Built with inspiration from:
- **TOGAF** - The Open Group Architecture Framework
- **Business Architecture Guild** - Business capability modeling
- **Enterprise Architecture** - Best practices from EA community
- **AI Development Community** - Feedback from practitioners using AI tools

---

## 📜 Changelog

### [1.0.0] - 2025-11-26

#### Added
- Initial release
- Quick Start template (10 sections)
- Full template (22 sections)
- Enterprise template (22+ sections)
- **Claude Code Agent** for AI-assisted template filling
- **Fact-checking system** - challenges vague/marketing content
- **Multi-language input** - any language in, English out
- Comprehensive documentation
- Tool suite (checklists, validators)

See [CHANGELOG.md](CHANGELOG.md) for full version history.

---

## 🚀 Get Started Now

### Fastest Way: Claude Code Agent ⭐

```bash
git clone https://github.com/Latentti/business-context-ai-template.git
cd business-context-ai-template
claude
/BizContext/start
```

### Manual Way

```bash
git clone https://github.com/Latentti/business-context-ai-template.git
cd business-context-ai-template/templates
cp business-context-full.yaml ../my-company-context.yaml
# Read docs/usage-guide.md and start filling
```

---

<div align="center">

**[⬆ Back to Top](#business-context-ai-template)**

Made with ❤️ by Ari Hietamäki & Latentti Oy for the AI development community

**Star ⭐ this repo if you find it useful!**

</div>
