# GitHub Copilot Agent Library

This repository contains **18 specialized AI agent personas** for GitHub Copilot CLI. Each agent is a domain expert providing guidance in technical or business areas.

## Project Architecture

**Agent Structure:**
- All agents live in [agents/](agents/) directory as `.agent.md` files
- Each agent follows the GitHub Copilot CLI agent format with YAML frontmatter
- Naming convention: kebab-case matching the agent's role (e.g., `technical-lead-archie.agent.md`)

**Required YAML Frontmatter:**
```yaml
---
name: agent-name        # Unique identifier used with @agent-name syntax
description: Brief description of when to use this agent
---
```

**Agent Categories:**
- **Technical Agents** (10): Architecture, testing, code quality, debugging, security, DevOps, Git, docs, API design, solution evaluation
- **Business Agents** (8): Project management, CEO/CFO/Sales/Marketing strategy, HR, customer success, supply chain

## Agent File Patterns

**Consistent Structure Across All Agents:**
1. **YAML frontmatter** with name and description
2. **Identity section** establishing persona and approach (e.g., "You are A.R.C.H.I.E...")
3. **Core principles/directives** defining behavior and philosophy
4. **Domain expertise** with specific technical or business areas
5. **Response structure** or workflow guidance
6. **Communication style** emphasizing educational, actionable advice

**Key Naming Pattern:**
Agents use memorable acronyms:
- A.R.C.H.I.E. (Architectural Counsel & Hands-on Implementation Expert)
- Q.A.I. (Quality Assurance Inspector)
- S.E.C. (Security Evaluation & Compliance)
- G.I.T. (Git Specialist)
- T.E.S.T. (Test Strategy Architect)

## Contributing New Agents

**When adding a new agent:**
1. Create `.agent.md` file in [agents/](agents/)
2. Include required YAML frontmatter (`name`, `description`)
3. Define clear specialization - avoid overlap with existing 18 agents
4. Follow established structure: identity → principles → expertise → response format
5. Use educational, mentoring tone that explains "why" behind recommendations
6. Add agent to README.md catalog with description and example invocation

**Testing Your Agent:**
```bash
# Install locally
mkdir -p ~/.github/agents
cp agents/your-agent.agent.md ~/.github/agents/

# Test in Copilot Chat
@your-agent-name Help me with [specific task]
```

## Installation & Usage

**User-level installation** (available in all projects):
```bash
mkdir -p ~/.github/agents
cp agents/*.agent.md ~/.github/agents/
```

**Workspace-level installation** (available in current project only):
```bash
mkdir -p .github/agents
cp agents/*.agent.md .github/agents/
```

**Invoking agents:**
- In chat: `@agent-name your question`
- CLI: `gh copilot chat --agent agent-name "your question"`
- Let Copilot auto-select agents based on context

## Key Files

- [README.md](README.md) - Complete documentation, agent catalog, usage examples
- [agents/](agents/) - All 18 agent definition files
- [LICENSE](LICENSE) - MIT License

## Conventions

**When modifying agents:**
- Keep descriptions concise but specific (avoid generic advice)
- Include concrete examples from relevant domains
- Focus on actionable patterns, not aspirational practices
- Reference official documentation (PEP 8, OWASP, etc.) where applicable
- Maintain consistent severity classification: [Critical], [Suggestion], [Question]

**Code Review Standards (from Q.A.I. agent):**
- Correctness, readability, performance, security, testability
- Provide line-specific feedback with explanations
- Link to style guides and best practices

**Git Commit Standards (from G.I.T. agent):**
- Conventional Commits format: `<type>[scope]: <description>`
- Types: feat, fix, docs, style, refactor, perf, test, build, ci, chore, revert
- Atomic commits (one logical change per commit)
- Explain WHY changes were made in commit body
