# GitHub Copilot CLI Agent Library

A curated collection of **18 specialized AI agent personas** for [GitHub Copilot CLI](https://docs.github.com/en/copilot/using-github-copilot/using-extensions/using-custom-agents). Each agent provides expert-level guidance in specific domains—from technical architecture to business strategy.

## Quick Start

### Installation

Copy agent files to your GitHub Copilot agents directory:

```bash
# For user-level agents (available across all projects)
mkdir -p ~/.github/agents
cp agents/*.agent.md ~/.github/agents/

# For workspace-level agents (available in current project only)
mkdir -p .github/agents
cp agents/*.agent.md .github/agents/
```

### Usage

GitHub Copilot CLI will automatically invoke agents when appropriate, or you can explicitly request an agent:

**Using the agent dropdown:**
- Select an agent from the agent dropdown in GitHub Copilot Chat

**Using slash commands:**
```bash
gh copilot chat --agent technical-lead-archie "Review my API design"
```

**In natural conversation:**
```
@technical-lead-archie Review my API design for the user authentication endpoint
@code-quality-inspector Check my recent changes before I commit
@github-commit-specialist Help me commit these authentication changes
```

---

## Agent Catalog

### Technical Agents

| Agent | File | Description |
|-------|------|-------------|
| **A.R.C.H.I.E.** | `technical-lead-archie.agent.md` | Technical lead for Cloud (AWS/GCP/Azure), Python, TypeScript, and Godot Engine. Provides architectural decisions, code reviews, and mentoring. |
| **A.P.I.** | `api-design-specialist.agent.md` | REST and GraphQL API design specialist. Covers resource modeling, versioning strategies, and OpenAPI documentation. |
| **T.E.S.T.** | `test-strategy-architect.agent.md` | Testing strategy architect for pytest, Jest, Vitest, Playwright, and Godot GUT. Designs test pyramids and fixes flaky tests. |
| **Q.A.I.** | `code-quality-inspector.agent.md` | Code review specialist analyzing correctness, readability, performance, security, and testability. |
| **D.E.B.U.G.** | `debugging-detective.agent.md` | Systematic debugging and root cause analysis. Investigates production issues, performance problems, and cryptic errors. |
| **S.E.C.** | `security-auditor.agent.md` | Security review and vulnerability detection. Identifies OWASP Top 10 issues, injection flaws, and auth weaknesses. |
| **D.E.V.O.P.S.** | `devops-sre-specialist.agent.md` | DevOps and SRE specialist for CI/CD, Kubernetes, Terraform, and infrastructure reliability. |
| **G.I.T.** | `github-commit-specialist.agent.md` | Git workflow expert. Creates conventional commits, organizes changes into atomic commits, and maintains repository hygiene. |
| **D.O.C.** | `technical-documentation-specialist.agent.md` | Technical writing specialist for API docs, architecture overviews, and code documentation. |
| **C.A.T.S.** | `technical-solution-advocate.agent.md` | Vendor evaluation and build-vs-buy analysis. Assesses TCO, lock-in risks, and technical proposals. |

### Business & Operations Agents

| Agent | File | Description |
|-------|------|-------------|
| **G.E.N.T.** | `project-manager-gent.agent.md` | Project manager for agile teams. Facilitates stand-ups, sprint planning, and blocker resolution. |
| **C.E.O.** | `ceo-strategist.agent.md` | Business strategy and executive guidance. Covers market analysis, competitive positioning, and growth strategy. |
| **C.F.O.** | `cfo-financial-strategist.agent.md` | Financial planning, budgeting, unit economics, and fundraising strategy. |
| **S.A.L.E.S.** | `sales-strategist.agent.md` | Sales process optimization, pipeline management, and go-to-market strategy. |
| **G.R.O.W.T.H.** | `marketing-growth-specialist.agent.md` | Marketing strategy, growth tactics, and brand positioning. |
| **C.S.M.** | `customer-success-specialist.agent.md` | Customer success, retention strategy, and churn prevention. |
| **H.R.** | `hr-people-strategist.agent.md` | Talent acquisition, organizational design, compensation, and culture development. |
| **I.N.V.** | `inventory-supply-chain-specialist.agent.md` | Supply chain optimization, inventory management, and logistics strategy. |

---

## Agent Details

### technical-lead-archie.agent.md

**A.R.C.H.I.E.** (Architectural Counsel & Hands-on Implementation Expert)

**Use when you need:**
- Cloud architecture design (AWS, GCP, Azure)
- Python performance optimization (FastAPI, Django)
- TypeScript/React architectural guidance
- Godot Engine game development expertise
- Code review with educational explanations

**Example invocation:**
```
@technical-lead-archie My Flask API is taking 3 seconds to respond. Can you optimize it?
```

---

### api-design-specialist.agent.md

**A.P.I.** (Application Programming Interface Specialist)

**Use when you need:**
- RESTful API resource modeling
- GraphQL schema design
- API versioning strategies
- OpenAPI/Swagger documentation
- REST vs GraphQL trade-off analysis

**Example invocation:**
```
@api-design-specialist Design pagination for our user list endpoint
```

---

### test-strategy-architect.agent.md

**T.E.S.T.** (Test Strategy Architect)

**Use when you need:**
- Test pyramid design for your project
- Flaky test diagnosis and remediation
- pytest fixture patterns
- Jest/Vitest/Playwright configuration
- Test coverage prioritization

**Example invocation:**
```
@test-strategy-architect Our E2E tests keep failing in CI. Can you help fix them?
```

---

### code-quality-inspector.agent.md

**Q.A.I.** (Quality Assurance Inspector)

**Use when you need:**
- Systematic code review before PR submission
- Performance bottleneck identification
- Security vulnerability detection
- Best practices validation (PEP 8, ESLint)
- React/TypeScript anti-pattern detection

**Example invocation:**
```
@code-quality-inspector Review my new authentication module
```

---

### debugging-detective.agent.md

**D.E.B.U.G.** (Debugging Detective)

**Use when you need:**
- Production bug investigation
- Stack trace analysis
- Performance degradation diagnosis
- Race condition identification
- Memory leak detection

**Example invocation:**
```
@debugging-detective We're getting random 500 errors in production. Can you investigate?
```

---

### security-auditor.agent.md

**S.E.C.** (Security Auditor)

**Use when you need:**
- OWASP Top 10 vulnerability scanning
- Authentication/authorization review
- Injection flaw detection (SQL, XSS, CSRF)
- Secrets and credential scanning
- Dependency vulnerability assessment

**Example invocation:**
```
@security-auditor Review our payment processing code before launch
```

---

### devops-sre-specialist.agent.md

**D.E.V.O.P.S.** (DevOps & SRE Specialist)

**Use when you need:**
- CI/CD pipeline design (GitHub Actions, GitLab CI)
- Kubernetes deployment configuration
- Terraform infrastructure as code
- Docker containerization
- Monitoring and alerting setup

**Example invocation:**
```
@devops-sre-specialist Set up GitHub Actions for our monorepo
```

---

### github-commit-specialist.agent.md

**G.I.T.** (Git Specialist)

**Use when you need:**
- Conventional commit message creation
- Atomic commit organization
- Git history cleanup before merge
- PR description writing
- Changelog generation

**Example invocation:**
```
@github-commit-specialist I've finished the OAuth feature. Help me commit my changes.
```

---

### technical-documentation-specialist.agent.md

**D.O.C.** (Documentation & Organization Conduit)

**Use when you need:**
- API reference documentation
- Architecture decision records (ADRs)
- README and onboarding guides
- Code docstrings and JSDoc
- System design documentation

**Example invocation:**
```
@technical-documentation-specialist Document our authentication flow
```

---

### technical-solution-advocate.agent.md

**C.A.T.S.** (Customer Advocate for Technical Solutions)

**Use when you need:**
- Build vs buy analysis
- Vendor proposal evaluation
- Total Cost of Ownership (TCO) calculation
- Cloud provider comparison
- Lock-in risk assessment

**Example invocation:**
```
@technical-solution-advocate Should we use Auth0 or build our own auth? Analyze the options.
```

---

### project-manager-gent.agent.md

**G.E.N.T.** (Generative Engagement & Navigation Tool)

**Use when you need:**
- Daily stand-up facilitation
- Sprint planning and retrospectives
- Blocker identification and escalation
- Project status reporting
- Meeting summaries and action items

**Example invocation:**
```
@project-manager-gent Prepare our sprint planning session
```

---

### ceo-strategist.agent.md

**C.E.O.** (Chief Executive Strategist)

**Use when you need:**
- Business strategy development
- Market opportunity analysis
- Competitive positioning
- Organizational prioritization
- Board presentation preparation

**Example invocation:**
```
@ceo-strategist Analyze our expansion into the European market
```

---

### cfo-financial-strategist.agent.md

**C.F.O.** (Chief Financial Strategist)

**Use when you need:**
- Financial modeling and projections
- Unit economics analysis (CAC, LTV)
- Budgeting and resource allocation
- Fundraising strategy
- Cash flow management

**Example invocation:**
```
@cfo-financial-strategist Model our runway with different growth scenarios
```

---

### sales-strategist.agent.md

**S.A.L.E.S.** (Sales Strategist)

**Use when you need:**
- Sales process optimization
- Pipeline management strategy
- MEDDIC/SPIN qualification frameworks
- Pricing strategy
- Go-to-market planning

**Example invocation:**
```
@sales-strategist Improve our enterprise sales qualification process
```

---

### marketing-growth-specialist.agent.md

**G.R.O.W.T.H.** (Marketing & Growth Specialist)

**Use when you need:**
- Growth strategy and experimentation
- Content marketing planning
- SEO and acquisition channels
- Brand positioning
- Campaign performance analysis

**Example invocation:**
```
@marketing-growth-specialist Plan our product launch campaign
```

---

### customer-success-specialist.agent.md

**C.S.M.** (Customer Success Manager)

**Use when you need:**
- Customer health scoring
- Churn prediction and prevention
- Onboarding journey design
- QBR preparation
- Expansion revenue strategy

**Example invocation:**
```
@customer-success-specialist Design our customer health score model
```

---

### hr-people-strategist.agent.md

**H.R.** (Human Resources Strategist)

**Use when you need:**
- Recruiting process optimization
- Compensation framework design
- Organizational structure planning
- Performance review systems
- Culture development

**Example invocation:**
```
@hr-people-strategist Design our engineering leveling framework
```

---

### inventory-supply-chain-specialist.agent.md

**I.N.V.** (Inventory & Network Virtuoso)

**Use when you need:**
- Inventory optimization
- Demand forecasting
- Warehouse/3PL evaluation
- Supply chain cost analysis
- Logistics network design

**Example invocation:**
```
@inventory-supply-chain-specialist Optimize our reorder points
```

---

## Customization

### Agent Configuration

GitHub Copilot CLI agents use YAML frontmatter for configuration:

```yaml
---
name: my-custom-agent
description: A specialized agent for specific domain expertise
---
```

**Required properties:**
- `name`: The unique identifier for your agent (used with `@agent-name` syntax)
- `description`: A clear, concise description of what the agent does

**Optional properties:**
- `tools`: Array of tools the agent can access (if omitted, agent has access to all tools)

### Tool Access Control

By default, agents have access to all available tools. To restrict tool access, specify the `tools` property:

```yaml
---
name: read-only-reviewer
description: Code reviewer with read-only access
tools: [read, search]
---
```

> **Note**: All 18 agents in this library use the default configuration (unrestricted tool access). Tool access control is available for custom agents that require scoped permissions for safety or compliance reasons. Consider restricting tools for agents that review external code or interact with untrusted inputs.

### Adding New Agents

1. Create a new `.agent.md` file in the `agents/` directory
2. Define clear specialization (avoid overlap with existing agents)
3. Include YAML frontmatter with `name` and `description`
4. Write comprehensive instructions defining the agent's role, expertise, and behavior
5. Test the agent by referencing it with `@agent-name` in Copilot Chat

**Example structure:**
```markdown
---
name: database-architect
description: Database design, query optimization, and schema migration specialist for PostgreSQL and MySQL
---

You are a database architecture specialist focused on...

[Agent instructions and behavior definitions]
```

---

## Contributing

This project is licensed under the **MIT License**.

### Quality Checklist

When contributing new agents or improving existing ones:

- [ ] YAML frontmatter includes required `name` and `description` properties
- [ ] Description clearly explains when to use the agent
- [ ] Agent has clear, non-overlapping specialization
- [ ] Core principles and expertise are domain-specific (not generic)
- [ ] Includes concrete examples and use cases from the domain
- [ ] File uses `.agent.md` extension
- [ ] Agent works correctly when invoked with `@agent-name` syntax
- [ ] Documentation is updated in README.md (if adding new agent)

### Contribution Guidelines

1. **Fork the repository** and create a feature branch
2. **Add or modify agents** following the established structure
3. **Test your changes** by installing agents locally and invoking them
4. **Update README.md** if adding new agents or changing functionality
5. **Submit a pull request** with a clear description of changes

---

## License

[MIT](LICENSE) - MIT License
