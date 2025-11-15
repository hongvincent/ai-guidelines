# CLAUDE.md - AI Assistant Guide for SANS AI Critical Security Guidelines

> **Language**: [English](CLAUDE.md) | [한국어](CLAUDE.ko.md)

## Repository Overview

This repository hosts the **SANS AI Critical Security Guidelines**, a living document that provides comprehensive security controls and best practices for AI implementations in enterprise environments. Published initially in March 2025, this is a collaborative, community-driven project designed to evolve with the rapidly changing AI security landscape.

**Current Version:** 1.1 (April 2025)
**Next Publication:** August 2025

## Repository Structure

```
ai-guidelines/
├── README.md                                    # Project overview and contribution guidelines
├── SANS_Critical_AI_Security_Guidelines_v1.1.md # Main guidelines document
├── figures/                                     # Supporting images
│   ├── figure1-data_protection_techniques.png
│   └── figure2-monitoring_best_practices.png
└── CLAUDE.md                                    # This file
```

## Mission and Purpose

The SANS AI Critical Security Guidelines aims to:

1. **Provide Point-in-Time Security Recommendations** - Capture current best practices for AI security as the field evolves
2. **Enable Risk-Based AI Implementation** - Help organizations implement AI safely using comprehensive security controls
3. **Serve the Global Cybersecurity Community** - Empower current and future cybersecurity practitioners worldwide
4. **Maintain Vendor Neutrality** - Provide unbiased, evidence-based security guidance

## Core Content Areas

The guidelines are organized into six critical categories:

### 1. Access Controls
- Model parameter protection
- Augmentation data security (RAG/VectorDB)
- Least privilege principles
- Zero trust integration

### 2. Data Protection
- Training data integrity
- Sensitive data safeguards
- Encryption strategies
- Data governance

### 3. Deployment Strategies
- Local vs. SaaS model hosting decisions
- IDE integration security
- Access control architecture
- Public model risks (HuggingFace, etc.)

### 4. Inference Security
- LLM guardrails
- Input/output validation and sanitization
- Prompt injection protection
- Modality and language considerations
- Encoding/compression attack vectors
- API usage monitoring

### 5. Monitoring
- Performance degradation detection
- Adversarial attack identification
- Anomaly detection
- Drift monitoring
- Inference refusal tracking

### 6. Governance, Risk, Compliance (GRC)
- Regular testing and tuning
- AI Bill of Materials (AIBOM)
- Model registries
- Regulatory framework compliance (EU AI Act, ELVIS Act, etc.)
- Agentic systems security
- Incident response for AI systems

## Development Workflow

### Branch Naming Convention

**Standard Format:** `lastname-monthyear`
**Example:** `bromiley-may2025`

**Special Format for Claude Code Sessions:** `claude/claude-md-<session-id>`
**Current Working Branch:** `claude/claude-md-mhzx8lc5xdybba2u-01SwqWScSEhch3zcWLRbfJYw`

### Contribution Process

1. **Clone** the repository
2. **Create** a feature branch following naming conventions
3. **Implement** changes to the Markdown document
4. **Add** supporting materials (images, diagrams, references)
5. **Push** changes to the feature branch
6. **Submit** a Pull Request for review
7. **Engage** with reviewers and iterate as needed

### Git Operations Best Practices

- Always use `git push -u origin <branch-name>` for first push
- Claude-specific branches must start with `claude/` and end with session ID
- Retry network failures up to 4 times with exponential backoff (2s, 4s, 8s, 16s)
- Prefer fetching specific branches: `git fetch origin <branch-name>`

## Content Standards and Guidelines

### What IS Allowed

✅ **Professional technical contributions** - Accurate, evidence-based security guidance
✅ **Referenced statements** - All facts backed by credible sources with links
✅ **Vendor-agnostic recommendations** - General best practices applicable across platforms
✅ **Clear documentation** - Well-formatted, structured content
✅ **Scope-aligned additions** - AI security-focused content
✅ **Updates to existing sections** - Improvements to accuracy and clarity

### What is NOT Allowed

❌ **Product promotion** - No proprietary content or product endorsements
❌ **Harmful language** - No biases or negative insinuations about products, companies, or individuals
❌ **Unsupported claims** - No statements without credible references
❌ **Off-topic content** - Must align with AI security focus
❌ **Copyright violations** - Only authorized content

### Quality Requirements

1. **Technical Accuracy** - Align with current industry standards
2. **Evidence-Based** - Include links or reports supporting claims
3. **Clear Context** - Provide explanations for all contributions
4. **Consistent Formatting** - Follow existing Markdown structure
5. **Mission Alignment** - Support SANS mission to empower cybersecurity practitioners

## Document Structure and Formatting

### Markdown Conventions

- **H1 (`#`)** - Main title only
- **H2 (`##`)** - Major sections (Overview, Control Categories, Conclusion, Glossary)
- **H3 (`###`)** - Control category names
- **H4 (`####`)** - Specific recommendations within categories
- **Bold** - Emphasis on key terms and frameworks
- **Italic** - Figure captions and references
- **Tables** - Regulatory frameworks and structured comparisons
- **Blockquotes (`>`)** - Extended commentary or expert insights

### Image References

Images are stored in `figures/` directory and referenced using relative paths:

```markdown
![Description](./figures/figure-name.png)
```

### External References

- Use hyperlinks for all external references
- Prefer stable, authoritative sources (OWASP, NIST, MITRE, research papers)
- Include context about why the reference is relevant

## Key Technical Terms (Glossary Reference)

Understanding these terms is essential when working with this document:

- **LLM (Large Language Model)** - Generative AI trained on massive datasets
- **RAG (Retrieval-Augmented Generation)** - LLMs enhanced with external vector databases
- **VectorDB** - Specialized database for semantic search in high-dimensional space
- **AIBOM (AI Bill of Materials)** - Record of datasets, models, code, and dependencies
- **Prompt Injection** - Adversarial attack to override model instructions
- **Inference Guardrails** - Policy filters on model inputs/outputs
- **Model Registry** - Centralized repository for ML model lifecycle management
- **Multimodal Model** - AI handling multiple data types (text, images, audio)
- **TEE (Trusted Execution Environment)** - Secure processor enclave for sensitive computations
- **Drift Monitoring** - Tracking model performance over time

## Working with This Repository as an AI Assistant

### Reading and Analysis Tasks

When asked to analyze or explain content:

1. **Reference specific sections** - Use H2/H3/H4 headings for navigation
2. **Cite line numbers** - When quoting, reference `SANS_Critical_AI_Security_Guidelines_v1.1.md:line_number`
3. **Cross-reference related sections** - Security controls often interconnect
4. **Acknowledge versioning** - Current version is 1.1; content is point-in-time

### Editing and Contribution Tasks

When making changes to the document:

1. **Maintain formatting consistency** - Match existing Markdown structure
2. **Preserve technical accuracy** - Verify claims against sources
3. **Add credible references** - Include hyperlinks for new claims
4. **Update version info carefully** - Don't change version numbers without authorization
5. **Respect vendor neutrality** - Remove any product-specific recommendations
6. **Check for scope alignment** - Ensure additions fit within AI security focus

### Common Tasks

**Adding a new security recommendation:**
1. Identify the appropriate control category (Access, Data, Deployment, Inference, Monitoring, GRC)
2. Create a new H4 heading with clear, actionable title
3. Provide context and rationale
4. Include technical implementation guidance
5. Add references to support recommendations

**Updating existing content:**
1. Read the full section for context
2. Verify current information is outdated or incomplete
3. Make minimal, targeted changes
4. Preserve the original tone and structure
5. Add references for new information

**Adding figures or diagrams:**
1. Save image files to `figures/` directory
2. Use descriptive filenames: `figure#-description.png`
3. Reference in document: `![Alt text](./figures/filename.png)`
4. Add caption with source attribution if applicable

## Regulatory and Framework References

The document tracks multiple AI security frameworks. When adding or updating regulatory information:

- **Check enactment dates** - Ensure accuracy
- **Link to official sources** - Use government or authoritative URLs
- **Summarize key concerns** - Focus on security implications
- **Consider geographic scope** - Note jurisdiction (EU, US, state-level, etc.)

Current frameworks covered:
- EU Artificial Intelligence Act
- ELVIS Act (US/Tennessee)
- Executive Order 14110 (US)
- Framework Convention on AI (Council of Europe)
- China's Generative AI Management Measures
- Israel's AI Policy
- California SB 1047
- Utah AI Policy Act

## Testing and Validation

Before submitting changes:

1. **Markdown validation** - Ensure proper syntax
2. **Link checking** - Verify all external URLs work
3. **Image verification** - Confirm images display correctly
4. **Cross-reference accuracy** - Check section references are correct
5. **Spell check** - Review for typos and grammatical errors
6. **Technical review** - Verify technical accuracy of security claims

## Commit Message Guidelines

Write clear, descriptive commit messages:

**Good examples:**
- "Add guidance on securing agentic AI systems"
- "Update EU AI Act enactment date and reference"
- "Fix broken OWASP link in inference security section"
- "Add new figure for model registry architecture"

**Poor examples:**
- "Updates" (too vague)
- "Fixed stuff" (unprofessional)
- "Added XYZ product recommendation" (violates vendor neutrality)

## Working with Pull Requests

When a PR is requested:

1. **Review all changes** - Read the full diff
2. **Check contribution guidelines** - Verify compliance
3. **Test links and images** - Ensure functionality
4. **Assess technical accuracy** - Verify security claims
5. **Provide constructive feedback** - Focus on improvement
6. **Suggest references** - If claims need support

## Common Pitfalls to Avoid

1. **Don't modify version numbers** - These are updated during official releases
2. **Don't add product endorsements** - Maintain vendor neutrality
3. **Don't skip references** - All claims need credible sources
4. **Don't ignore existing structure** - Follow established formatting
5. **Don't duplicate content** - Cross-reference instead
6. **Don't use casual language** - Maintain professional tone
7. **Don't add unverified claims** - Verify all technical assertions

## Resources for Research

When researching AI security topics, consult:

- **OWASP AI Exchange** - https://owaspai.org/
- **MITRE ATLAS** - AI threat knowledge base
- **NIST AI Risk Management Framework** - https://www.nist.gov/itl/ai-risk-management-framework
- **Cloud Security Alliance** - AI security research
- **Academic Research** - arXiv, conference papers (NeurIPS, ICML, etc.)
- **Vendor Security Blogs** - Technical implementation guidance (Anthropic, OpenAI research blogs)

## Collaboration and Community

This is a **living document** maintained by the cybersecurity community. Key principles:

- **Respectful collaboration** - Engage professionally with all contributors
- **Knowledge sharing** - Help others understand security implications
- **Continuous improvement** - Embrace feedback and iteration
- **Mission focus** - Always align with empowering cybersecurity practitioners
- **Transparency** - Document rationale for significant changes

## Version History Context

**v1.1 (April 2025)** - Current version
- Added agentic systems security section
- Expanded incident response guidance
- Updated regulatory framework table
- Enhanced monitoring best practices

**v1.0 (March 2025)** - Initial release
- Established six control categories
- Defined core security recommendations
- Created glossary of terms

**Next Update (August 2025)** - Planned
- Expected to incorporate community contributions
- May address emerging threats and technologies

## Questions and Support

For questions about:

- **Repository structure** - Refer to this file
- **Contribution process** - See README.md
- **Technical content** - Read the main guidelines document
- **Git workflow** - Follow standard Git practices with branch naming conventions
- **SANS mission** - Visit https://www.sans.org/mission/

## Final Notes for AI Assistants

When working in this repository:

1. **Understand the mission** - This document empowers cybersecurity professionals
2. **Respect the process** - Follow established workflows and guidelines
3. **Maintain quality** - Uphold high standards for technical accuracy
4. **Stay current** - AI security evolves rapidly; verify information currency
5. **Be helpful** - Support contributors in creating valuable security guidance
6. **Document changes** - Use clear commit messages and detailed PR descriptions
7. **Ask when uncertain** - Better to clarify than to introduce errors

This repository represents a critical resource for the global cybersecurity community. Every contribution should honor that responsibility.

---

*Last Updated: November 2025*
*Document Version: 1.0*
*For Repository Version: SANS AI Critical Security Guidelines v1.1*
