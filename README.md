# Anti VibeCoding

> Enforce structured, disciplined, engineering-first thinking for any project or feature.

A universal skill that prevents "vibe coding" — the tendency to write code without clear requirements, architecture, or plan — and guides users through a rigorous engineering workflow.

**Works with:** Claude Code, Cursor, Windsurf, VS Code Copilot, GitHub Copilot, and any AI coding assistant.

---

## What It Does

When activated, this skill transforms your AI assistant into a **senior software engineer and system architect** who:

- Refuses to proceed with vague or incomplete requirements
- Asks clarifying questions before assuming anything
- Enforces structured thinking over speed
- Challenges weak ideas and incomplete specifications
- Enforces the use of PRD and TSD templates

---

## Quick Start

### Claude Code (Recommended)

```bash
# Via git clone
git clone https://github.com/Sharda2004196/anti-vibecoding.git ~/.claude/skills/anti-vibecoding

# Or manually: Copy this repo to ~/.claude/skills/anti-vibecoding/
```

Restart Claude Code, then activate with `/anti-vibecoding`

---

### Cursor

**Option 1: Rules file**
```bash
mkdir -p .cursor/rules
cp anti-vibecoding/SKILL.md .cursor/rules/anti-vibecoding.md
```
Then add to Cursor: Settings → Rules for AGENTS → Add Rule → Select `anti-vibecoding.md`

**Option 2: MCP Server (if available)**
Add to Cursor's MCP servers configuration.

---

### Windsurf (Codeium)

Add `SKILL.md` content to Windsurf workspace instructions:
1. Open Windsurf Settings → Workspace
2. Add custom instructions or load from file

---

### VS Code Copilot / antigravity

**Option 1: Custom Instructions**
1. VS Code Settings → Extensions → Copilot → Custom Instructions
2. Paste `SKILL.md` content

**Option 2: Repository-level**
```bash
mkdir -p .github
cp anti-vibecoding/SKILL.md .github/copilot-instructions.md
```

---

### GitHub Copilot (Codex / Agent Mode)

```bash
mkdir -p .github
cp anti-vibecoding/SKILL.md .github/copilot-instructions.md
```

---

### npx / npm (For Node.js projects)

```bash
# Clone the repo
npx degit Sharda2004196/anti-vibecoding anti-vibecoding

# Then follow platform-specific setup above
```

---

### Other AI Assistants

1. Copy `SKILL.md` contents
2. Paste into your AI assistant's system prompt/instructions
3. Keep templates in `/templates` folder for reference

---

## Usage

Activate the skill by typing:

```
/anti-vibecoding
```

Or simply explain what you're working on — the skill activates automatically when:

- Working on any software project or feature
- Creating a PRD or TSD
- Asking for structured, engineering-first guidance

---

## New vs Existing Projects

This skill works for **both new AND existing projects**:

| Project State | Where to Start |
|---------------|----------------|
| Brand new project | Phase 1 (Problem Definition) |
| Partial requirements | Phase 2-3 (Fill gaps) |
| Code exists, no docs | Phase 4 (Document architecture) |
| Working system, needs changes | Phase 7 (Review edge cases) |
| Bug fix needed | Phase 7 (Analyze failures) |

---

## The Workflow

Every project or feature follows this mandatory sequence:

```
1. Problem Definition → 2. Requirements Breakdown → 3. Clarification Phase
       ↓                      ↓                         ↓
4. System Design   → 5. Tech Stack Justification → 6. Implementation Planning
       ↓                      ↓                         ↓
7. Edge Cases & Constraints → 8. Testing Strategy → [Code Generation]
```

### Phase Details

| Phase | Purpose |
|-------|---------|
| **Problem Definition** | What are we building? Who is it for? What problem does it solve? |
| **Requirements Breakdown** | Functional and non-functional requirements |
| **Clarification Phase** | Targeted questions, identify ambiguities |
| **System Design** | Architecture, components, data flow |
| **Tech Stack Justification** | Technology choices with trade-offs explained |
| **Implementation Planning** | Modular steps, milestones, deliverables |
| **Edge Cases** | Failure scenarios, limits, assumptions |
| **Testing Strategy** | Unit, integration, and system testing |

---

## Templates

The skill uses standardized templates for documentation:

- **PRD Template:** `templates/prd.md` — Product Requirement Document
- **TSD Template:** `templates/tsd.md` — Technical Specification Document

Both templates are automatically referenced when generating documentation.

---

## Core Rules

1. **Never proceed with incomplete requirements** — Always ask for clarification first
2. **Always use templates** — PRD and TSD must follow the defined formats
3. **Challenge weak inputs** — Point out ambiguities, trade-offs, and missing information
4. **Justify decisions** — Every technology choice must have reasoning
5. **No coding without a plan** — Architecture and implementation plan come first

---

## Example Interaction

**User:** "Build a login system"

**Anti-VibeCoding Response:**
> "Before we start, I need clarification on the login system requirements:
>
> 1. **Authentication method:** Username/password, OAuth, SSO, or multi-factor?
> 2. **User management:** Self-registration, admin-created accounts, or both?
> 3. **Security requirements:** Password hashing algorithm? Session timeout? Rate limiting?
> 4. **Integration:** Database type? Existing user store to connect to?
>
> Please provide these details so I can create a proper PRD and TSD before any implementation."

---

## Contributing

Contributions welcome! Please see [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines.

---

## License

MIT License — See [LICENSE](LICENSE) for details.

---

## Related

- [PRD Template](templates/prd.md)
- [TSD Template](templates/tsd.md)
- [Claude Code Skills Documentation](https://docs.anthropic.com/en/docs/claude-code)