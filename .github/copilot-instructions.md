# GitHub Copilot Instructions - AI-Driven Development Framework

**🎯 PRIMARY INSTRUCTION:** Read `.ai/00_START_HERE.md` first. This file supplements it.

---

## ⚡ Quick Start (2 minutes)

You're working in an **AI-assisted development framework** designed for context persistence across multiple chat sessions.

### � On Every New Session:
1. **Go to:** `.ai/00_START_HERE.md`
2. **Follow the initialization steps** (it takes 5 minutes)
3. **Announce project status** using the template provided
4. **Then start working**

**That's it.** The `.ai/` folder contains everything you need.

---

## 📁 File Structure Overview

All project coordination lives in `.ai/`:

| Folder | Purpose |
|--------|---------|
| `.ai/planning/` | Architecture, tech stack, design decisions |
| `.ai/requirements/` | Full requirements and phase specifications |
| `.ai/phases/` | Active phase folders with tasks and progress |
| `.ai/templates/` | Copy these to create new phases/tasks |

**Source code** lives in `src/`, `tests/`, `docs/` — separate from metadata.

---

## 🧠 Core Framework Philosophy

This framework works through **three disciplines:**

### 1. **Initialization Protocol**
Every session starts by reading `.ai/00_START_HERE.md`. This establishes context and ensures you know:
- What phase/task you're on
- What changed since last session
- Any blockers or decisions

### 2. **Documentation Discipline**
After every task, **immediately** update (in order):
- ✅ Task file (status, date)
- ✅ `PHASE_STATUS.md` (task count)
- ✅ `MASTER_PROGRESS.md` (overall %)
- ✅ `MEMORY.md` (if decisions made)

**Why?** Next session's context depends on these files being current.

### 3. **Testing Requirement**
Never mark a task "Completed" without:
- Creating `TEST_PLAN.md` with specific test steps
- Having **user validate tests** (critical step)
- Updating all tracking files after user confirms

---

## 🏗️ Architecture at a Glance

### Three Documentation Layers:
1. **Planning:** `.ai/planning/` — Design decisions, tech choices
2. **Requirements:** `.ai/requirements/` — What each phase delivers
3. **Execution:** `.ai/phases/` — Progress tracking, task details

### Core Decisions (Why This Structure Works):
- **Separation of concerns** prevents planning from mixing with execution status
- **File-based system** works with any AI (GitHub Copilot, Claude, ChatGPT, Gemini)
- **Task-based breakdown** (2-8 hours each) makes progress measurable and testable
- **MEMORY.md as bridge** preserves decisions across sessions
- **.ai/ folder separate from src/** keeps metadata organized, code clean

See `.ai/planning/ARCHITECTURE.md` for detailed system design.

---

## 📊 The Task Lifecycle

```
Not Started → In Progress → Testing → Completed
```

### Starting a Task:
1. Update task file status to "In Progress"
2. Update `PHASE_STATUS.md` and `MASTER_PROGRESS.md`
3. Implement code with comments
4. Log decisions in `MEMORY.md`

### Finishing a Task:
1. Create `TEST_PLAN.md` (prerequisites, steps, expected results, edge cases)
2. Mark task status "Testing"
3. **User validates tests** (don't skip this)
4. After user confirms: update all tracking files
5. Mark status "Completed"

---

## 💾 MEMORY.md: Your Session Bridge

Log **every decision** in `.ai/MEMORY.md`. Next session reads it and stays in context.

### What to Log:

**Technical Decisions** (e.g., framework choice):
```markdown
| 2025-11-26 | Use framework templates for structure | Ensures consistency | Simplifies onboarding |
```

**Issues & Solutions** (e.g., when you hit a blocker):
```markdown
| 2025-11-26 | Phase folder unclear for users | Created templates in RULES.md | All users can follow |
```

**Dependencies Installed:**
```markdown
| 2025-11-26 | React 18.2 | UI framework for frontend | Phase 1 |
```

**Database/API/Config Changes:**
```markdown
| 2025-11-26 | users table | Added role column | Updated schema in DATABASE_SCHEMA.md |
```

---

## 🛠️ Before Adding New Technology

1. **Check** `.ai/planning/TECH_STACK.md` — Is it already listed?
2. **If new:** Log decision in `MEMORY.md` with rationale
3. **Update** `TECH_STACK.md` with justification
4. **Then** proceed with installation

This prevents tech sprawl and keeps the stack coherent.

---

## 🚨 When Things Go Wrong

### If Blocked:
1. **Log immediately** in `MEMORY.md` → "Issues and Solutions"
2. Mark task as "Blocked" in task file
3. Update `PHASE_STATUS.md` with blocker note
4. Propose solution to user with full context

### If You Find a Bug:
1. Log in `MEMORY.md` with timestamp and details
2. Create fix (or mark task "Blocked")
3. Add regression test to `TEST_PLAN.md`
4. Document the lesson learned

---

## ✅ File Update Checklist (After Every Task)

- [ ] Task file: status updated, completion date added
- [ ] `PHASE_STATUS.md`: task count incremented, % recalculated
- [ ] `MASTER_PROGRESS.md`: current task updated, overall % recalculated
- [ ] `MEMORY.md`: decisions/issues logged (if applicable)

**This is non-negotiable.** Context persistence depends on disciplined file updates.

---

## 💡 Code Standards

### General:
- Clean, readable code — names are self-documenting
- DRY principle — extract to functions/components
- Comments explain *why*, not *what*
- Consistent formatting per project rules

### Error Handling:
- Try-catch blocks around risky operations
- Meaningful error messages (not generic)
- Log errors with context
- Graceful degradation

### Security:
- Never hardcode credentials/secrets
- Validate all user inputs
- Sanitize data before storing
- Use environment variables for config
- Implement auth/authz properly

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

## 🎓 Key Files Reference

**Read these to understand the project:**
- **`.ai/PROJECT_CONTEXT.md`** — What is this project? Who uses it?
- **`.ai/RULES.md`** — Complete framework rules
- **`.ai/planning/ARCHITECTURE.md`** — How components work together
- **`.ai/planning/TECH_STACK.md`** — Technology choices and justification

**Update these after work:**
- **Current task file** — Status, completion date, notes
- **`.ai/MEMORY.md`** — Decisions, issues, learnings
- **`.ai/phases/phase-XX/PHASE_STATUS.md`** — Task progress
- **`.ai/MASTER_PROGRESS.md`** — Overall project metrics

---

## ❓ Common Questions

**Q: Where do I start?**  
A: `.ai/00_START_HERE.md` — read it first, every session.

**Q: How do I know what to do?**  
A: Open your current task file in `.ai/phases/phase-XX/tasks/TASK_XXX.md`

**Q: What if I'm confused?**  
A: Read `.ai/RULES.md` — it has everything.

**Q: How do I preserve context between sessions?**  
A: Update `.ai/MEMORY.md` with every decision/issue/learning.

---

## 🚀 You're Ready

1. **Go to:** `.ai/00_START_HERE.md`
2. **Follow it exactly**
3. **Come back here** if you have questions

---

**Framework Version:** 1.0  
**Compatible With:** GitHub Copilot, Claude, ChatGPT, Gemini, any AI assistant  
**Last Updated:** 2025-11-26
