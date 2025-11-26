# GitHub Copilot Instructions - AI-Driven Development Framework

## 🎯 Project Identity
This is an **AI-Driven Development Framework** — a universal, reusable template for AI-assisted software development that maintains context and tracks progress across multiple chat sessions.

**Key Purpose:** Enable systematic, context-persistent development with any AI assistant (Copilot, Claude, ChatGPT, Gemini, etc.)

---

## 🚀 Every New Session: The 5-Minute Initialization

Before writing any code or making decisions, **always** follow this sequence in order:

1. **Read** `.ai/00_START_HERE.md` — Quick orientation on current status
2. **Read** `.ai/RULES.md` — Framework rules and workflows (your development bible)
3. **Check** `.ai/MASTER_PROGRESS.md` — What phase/task are we on?
4. **Review** `.ai/MEMORY.md` — Recent decisions and issues (at least last 5 entries)
5. **Open** Current task file in `.ai/phases/phase-0X-name/tasks/TASK_XXX.md`

**After initialization, announce:**
```
📊 PROJECT STATUS
Project: [Name from PROJECT_CONTEXT.md]
Phase: [X/Y] - [Phase Name]  
Task: [XXX] - [Task Name]
Status: [Current Status]
Progress: [Overall %]

Ready to work. What would you like to do?
```

This isn't optional — context persistence depends on reading these files.

---

## 📁 Critical File Locations & When to Read Them

| File | When to Read | Why |
|------|--------------|-----|
| `.ai/00_START_HERE.md` | Every session start | Orients you to current context |
| `.ai/RULES.md` | Session start (refresh) | Contains all workflow rules |
| `.ai/MASTER_PROGRESS.md` | Before each task | Know what phase/task you're on |
| `.ai/MEMORY.md` | Session start (recent entries) | Know past decisions/issues |
| `.ai/PROJECT_CONTEXT.md` | On first session only | Understand project goals |
| `.ai/phases/phase-0X-name/PHASE_STATUS.md` | Before phase work | Track tasks in current phase |
| Current task file | When starting work | Get detailed task requirements |
| `.ai/planning/TECH_STACK.md` | Before adding dependencies | Check approved technologies |

**Note:** This framework IS a template project. When you start a real project, you'll follow the exact same file structure above, but with your project's data filled in. The framework itself demonstrates all the patterns you'll replicate.

---

## 🔄 The Task Lifecycle: What Success Looks Like

Every task follows this flow:

```
Not Started → In Progress → Testing → Completed
```

### When Starting a Task:
1. Update task file: change status to "In Progress"
2. Update `.ai/phases/phase-0X/PHASE_STATUS.md` with start time
3. Update `.ai/MASTER_PROGRESS.md` 
4. Implement code with meaningful comments
5. Log any decisions in `.ai/MEMORY.md` as you go

### When Finishing a Task:
1. **Generate TEST_PLAN.md** with manual test steps and expected results
2. Change task status to "Testing"
3. Provide clear test instructions to user
4. **Wait for user to validate tests** (don't skip this step)
5. After user confirms:
   - Update task: status = "Completed", add completion date
   - Update `PHASE_STATUS.md`: increment completed task count
   - Update `MASTER_PROGRESS.md`: recalculate percentages
   - Update `MEMORY.md` with learnings (if applicable)

---

## 🧠 The Memory System: How to Preserve Context

The `.ai/MEMORY.md` file is your session bridge. **Always log**:

### Technical Decisions
Add to "Key Decisions" table when you make a choice:
```markdown
| 2025-11-26 | Use framework templates for structure | Ensures consistency across all projects | Simplifies onboarding, faster setup | AI |
| 2025-11-26 | Store all phase/task tracking in .ai/ | Keeps source code clean, centralizes metadata | Easy to find progress info | AI |
| 2025-11-26 | Require user testing before task completion | Catches implementation issues early | Prevents bugs from compounding | AI |
```

### Issues You Encounter
Add to "Issues and Solutions" when you hit a blocker:
```markdown
| 2025-11-26 | Task marked complete but user testing not done | Established testing requirement before completion | MEMORY.md, RULES.md | Always wait for user validation |
| 2025-11-26 | Phase folder creation unclear for first-time users | Created templates and step-by-step in RULES.md | All phase files | Reference RULES.md for sequence |
```

### New Dependencies
Add to "Dependencies Installed" whenever you `npm install` or add packages:
```markdown
| 2025-11-26 | Framework templates | N/A | Project scaffolding structure | Phase 0 |
| 2025-11-26 | GitHub Actions CI/CD | N/A | Automated testing/deployment | Phase 0 |
```

### Database/API/Config Changes
Log immediately in appropriate section if you modify structure or endpoints:
```markdown
| 2025-11-26 | .ai/ directory structure | Added `.ai/planning/` for architecture docs | Centralizes design decisions | Phase 0 |
| 2025-11-26 | MEMORY.md sections | Added "Learnings & Best Practices" section | Improved knowledge retention | Phase 0 |
```

**Why?** Next session, the AI (you) reads this and knows the context. Without it, history is lost.

**Real-World Examples from This Framework:**
- Decision: "Chose three-layer doc structure (Planning/Requirements/Execution)" → Makes it clear why files are organized this way
- Issue: "First-time users confused about which file to read first" → Solution: "Created 00_START_HERE.md as entry point"
- Lesson: "Context persistence requires disciplined file updates, not AI intelligence" → Apply this to every project you work on

---

## ⚙️ Tech Stack Management: Before You Add New Tech

Before installing a package or adopting a new tool:

1. **Check** `.ai/planning/TECH_STACK.md` — Is it already listed?
2. **If new:** Log decision in `.ai/MEMORY.md` → "Key Decisions" table
3. **Add to** `.ai/planning/TECH_STACK.md` with justification
4. **Only then** proceed with installation

This prevents tech sprawl and ensures coherent architecture.

---

## 🧪 Testing Requirements: Non-Negotiable

After implementing a task:

1. **Create `TEST_PLAN.md`** in the task folder with:
   - Prerequisites (setup, test data, environment)
   - Manual test steps (numbered, specific)
   - Expected results (what should happen)
   - Edge cases (boundary conditions, error scenarios)
   - Pass/fail criteria

2. **User must manually test** — This validates your implementation
3. **Only mark "Completed"** after user confirms tests pass

No shortcuts. Testing is how we catch issues before they compound.

---

## 📝 Mandatory Updates After Every Task

After a task is completed, **in this order**:

1. ✅ Task file: Update status, add completion date, add notes
2. ✅ `PHASE_STATUS.md`: Increment completed task count, recalculate %
3. ✅ `MASTER_PROGRESS.md`: Update current task, recalculate overall %
4. ✅ `MEMORY.md`: Log any decisions/issues (if applicable)
5. ✅ Tech files: Update `TECH_STACK.md`, `DATABASE_SCHEMA.md`, `API_DESIGN.md` (if modified)

**Don't skip this.** These updates are how the next session knows what happened.

---

## 🏗️ Project Architecture Overview

This framework maintains three parallel documentation systems:

### 1. **Planning Layer** (`.ai/planning/`)
- `ARCHITECTURE.md` — How components interact
- `TECH_STACK.md` — Technology choices and rationale
- `DATABASE_SCHEMA.md` — Data model and relationships
- `API_DESIGN.md` — API endpoints and specifications

### 2. **Requirements Layer** (`.ai/requirements/`)
- `MAIN_REQUIREMENTS.md` — Full project requirements
- `phases/PHASE_0X_[NAME].md` — What each phase must deliver

### 3. **Execution Layer** (`.ai/phases/phase-0X-name/`)
- `PHASE_STATUS.md` — Progress tracking within phase
- `tasks/TASK_XXX_NAME.md` — Individual task details and status
- `testing/` — Test plans and results per phase

**Why this structure?** Separation of concerns. Planning doesn't get tangled with execution status.

### Core Framework Decisions (Recorded in MEMORY.md When This Was Built)

| Decision | Rationale |
|----------|-----------|
| **Three-layer documentation** | Planning → Requirements → Execution prevents confusion between design intent and progress tracking |
| **Task-based breakdown** | Each task is 2-8 hours, independently testable, validatable before moving forward |
| **Mandatory file updates after each task** | Context persistence across sessions depends on disciplined documentation, not AI intelligence |
| **User validation before "Completed"** | Catches issues early; prevents bugs from compounding into next phase |
| **MEMORY.md as session bridge** | Records decisions, issues, and learnings so next AI session has full context |
| **.ai/ folder separate from src/** | Keeps project metadata organized; source code stays clean |
| **Universal compatibility** | Framework works with any AI (Copilot, Claude, ChatGPT, Gemini) because it's file-based, not API-dependent |

These decisions guided the framework's design. When you start your own project using this template, you'll create similar decision entries in MEMORY.md for YOUR project's choices.

---

## 🚨 Error Recovery: When Things Go Wrong

### If You Get Stuck:
1. **Document immediately** in `.ai/MEMORY.md` → "Issues and Solutions"
2. **Mark task** as "Blocked" in task file
3. **Update** `PHASE_STATUS.md` with blocker notation
4. **Propose solution** to user with full context
5. **Wait for approval** on major changes
6. **Implement fix** and remove blocker status

### If You Discover a Bug:
1. Log in `MEMORY.md` with timestamp and details
2. Create fix (or mark task as "Blocked")
3. Add regression test case to `TEST_PLAN.md`
4. Document lesson learned

---

## 💡 Code Standards for This Project

### General Principles
- **Clean, readable code** — Variable/function names are self-documenting
- **DRY** — Don't Repeat Yourself; extract to functions/components
- **Comments for complexity** — Explain the "why", not the "what"
- **Consistent formatting** — Use project's lint rules

### Error Handling
- Try-catch blocks around risky operations
- Meaningful error messages (not generic)
- Log errors with context
- Graceful degradation (don't crash the app)
- User-friendly messages in UI

### Security (Minimum Standards)
- **Never hardcode** credentials or secrets
- **Validate all inputs** from users/external sources
- **Sanitize** data before storing or displaying
- **Use environment variables** for configuration
- **Implement auth/authz** properly before deployment

---

## 📊 Progress Calculation: How We Measure

### Task Progress (within a phase)
```
Phase % = (Completed Tasks / Total Tasks) × 100
```

### Overall Project Progress
```
Project % = (Sum of all Phase % × Phase Weight) / 100
```

### Time Tracking
- Log estimated hours in task file
- Update actual hours after completion
- Compare vs. estimate to improve future estimates

---

## ✅ Completion Checklist: Task is Done When

- [ ] Code implemented and working
- [ ] Comments added for complex logic
- [ ] `TEST_PLAN.md` created with specific test steps
- [ ] User manually validated tests
- [ ] Task file updated (status = "Completed", date filled)
- [ ] `PHASE_STATUS.md` updated (task count incremented)
- [ ] `MASTER_PROGRESS.md` updated (progress recalculated)
- [ ] `MEMORY.md` updated (decisions/issues logged, if any)

### Phase is Complete When
- [ ] All tasks completed and tested
- [ ] `PHASE_STATUS.md` shows 100%
- [ ] Phase documentation complete
- [ ] `MASTER_PROGRESS.md` updated
- [ ] Ready to move to next phase

---

## 🗣️ Communication Patterns

### Session Start
Announce current status with the 5-line status summary.

### During Work
- Explain what you're implementing
- Ask for clarification when requirements are ambiguous
- Propose solutions before making major architectural changes
- Report blockers immediately

### Session End
```
📋 SESSION SUMMARY
✅ Completed: [List tasks]
📝 Updated: [List files]
⏭️ Next Steps: [What's coming]
🚨 Blockers: [Any blockers, or "None"]
```

---

## ⚠️ Common Pitfalls to Avoid

### ❌ DON'T
- Skip file initialization at session start
- Mark tasks "Completed" without user testing
- Add new tech without logging in `MEMORY.md`
- Forget to update progress files
- Make architectural decisions without documenting rationale
- Lose context by not reading `MEMORY.md`

### ✅ DO
- Read framework files every session
- Wait for user validation on tests
- Log all decisions and issues
- Update files systematically after each task
- Ask for approval on major changes
- Use this document as your reference

---

## 🎓 Quick Reference: Files You'll Edit Most

1. **Current task file** — Status updates, implementation details
2. **`.ai/MEMORY.md`** — Decisions, issues, learnings
3. **`.ai/phases/phase-0X/PHASE_STATUS.md`** — Task progress
4. **`.ai/MASTER_PROGRESS.md`** — Overall metrics
5. **`.ai/planning/` files** — Architecture, tech stack, API changes

---

## 📌 Key Files to Understand First

- **`.ai/PROJECT_CONTEXT.md`** — What is this project? Who uses it? What's success?
- **`.ai/planning/ARCHITECTURE.md`** — How do components work together?
- **`.ai/planning/TECH_STACK.md`** — What technologies are approved?
- **Current phase folder** — What are we building this phase?

Read these before writing production code.

---

## 🚀 Start Working

Once you've read the initialization files and understand current status:

1. Open the current task file
2. Follow its acceptance criteria
3. Implement with comments
4. Create test plan
5. Wait for user validation
6. Mark complete and update all tracking files

**Remember:** The framework works because context is preserved, not because of AI capability. Follow the system, and projects progress steadily.

---

**Framework Version:** 1.0  
**Compatible With:** GitHub Copilot, Claude, ChatGPT, Gemini, any AI assistant  
**Last Updated:** 2025-11-26
