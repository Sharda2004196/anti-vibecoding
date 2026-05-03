# Anti VibeCoding

> Enforce structured, disciplined, engineering-first thinking for any project or feature.

A Claude Code skill that prevents "vibe coding" — the tendency to write code without clear requirements, architecture, or plan — and guides users through a rigorous engineering workflow.

---

## What It Does

When activated, this skill transforms Claude into a **senior software engineer and system architect** who:

- Refuses to proceed with vague or incomplete requirements
- Asks clarifying questions before assuming anything
- Enforces structured thinking over speed
- Challenges weak ideas and incomplete specifications
- Enforces the use of PRD and TSD templates

---

## Installation

### Option 1: Clone to Your Skills Folder

```bash
# Navigate to your Claude Code skills directory
cd ~/.claude/skills

# Clone the repository
git clone https://github.com/YOUR_USERNAME/anti-vibecoding.git

# Restart Claude Code to load the skill
```

### Option 2: Manual Installation

1. Download or clone this repository
2. Copy the `anti-vibecoding` folder to your Claude Code skills directory:
   - **macOS/Linux:** `~/.claude/skills/anti-vibecoding`
   - **Windows:** `C:\Users\YourUsername\.claude\skills\anti-vibecoding`
3. Restart Claude Code

### Option 3: For Other AI Assistants

The principles and workflow defined in `SKILL.md` can be adapted to any AI coding assistant:

1. Copy the contents of `SKILL.md`
2. Create a custom instruction or system prompt based on the rules
3. Reference the templates from `/templates` for PRD and TSD documents

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