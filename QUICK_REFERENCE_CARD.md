# 🎯 Framework Quick Reference Card

## 📍 You Are Here
```
d:\Web Development\GithubCopilotTest\
```

---

## 🎬 Start Now (Choose Your Path)

### Path A: Brand New Project (Recommended First)
```
1. Open: README_FRAMEWORK_INDEX.md ← Navigation Guide
2. Read: FRAMEWORK_SETUP_COMPLETE.md ← Setup Instructions
3. Edit: .ai/PROJECT_CONTEXT.md ← Your Project Details
4. Fill: .ai/requirements/MAIN_REQUIREMENTS.md ← Your Requirements
5. Plan: .ai/planning/*.md ← Architecture Decisions
6. Ready: Create phases in .ai/phases/
```

### Path B: I Want to Understand First
```
1. Read: README_FRAMEWORK_INDEX.md ← Overview
2. Study: .ai/00_START_HERE.md ← For AI Agents
3. Learn: .ai/RULES.md ← How Framework Works
4. Explore: .ai/templates/ ← See What You'll Create
5. Customize: .ai/PROJECT_CONTEXT.md
```

### Path C: Use with AI Right Away
```
1. Give AI: .ai/RULES.md ← Read This First
2. Give AI: .ai/PROJECT_CONTEXT.md ← Your Project
3. Give AI: .ai/requirements/MAIN_REQUIREMENTS.md ← Requirements
4. Command: "Start with Phase 1, Task 1"
5. AI Will: Follow RULES.md systematically
```

---

## 📂 Directory Map (One-Liner Each)

| Path | Purpose | Status |
|------|---------|--------|
| `README_FRAMEWORK_INDEX.md` | File index & navigation | ⭐ START HERE |
| `FRAMEWORK_SETUP_COMPLETE.md` | Setup guide | ⭐ START HERE |
| `.ai/00_START_HERE.md` | AI agent quick start | Read 1st per session |
| `.ai/RULES.md` | Framework rules & workflow | Read 1st per session |
| `.ai/PROJECT_CONTEXT.md` | Project info template | Edit first |
| `.ai/MEMORY.md` | Decision & learning tracker | Maintain continuously |
| `.ai/MASTER_PROGRESS.md` | Overall project progress | Update after tasks |
| `.ai/QUICK_START_INSTRUCTIONS.md` | Agent quick reference | Reference when stuck |
| `.ai/requirements/MAIN_REQUIREMENTS.md` | Full requirements | Create during planning |
| `.ai/planning/TECH_STACK.md` | Technology choices | Create during planning |
| `.ai/planning/ARCHITECTURE.md` | System design | Create during planning |
| `.ai/planning/DATABASE_SCHEMA.md` | Database structure | Create during planning |
| `.ai/planning/API_DESIGN.md` | API specifications | Create during planning |
| `.ai/templates/TASK_TEMPLATE.md` | Task template | Copy for each task |
| `.ai/templates/PHASE_TEMPLATE.md` | Phase template | Copy for each phase |
| `.ai/templates/TEST_PLAN_TEMPLATE.md` | Test plan template | Copy for each test |
| `.ai/templates/IMPLEMENTATION_PLAN_TEMPLATE.md` | Implementation template | Copy for each phase |

---

## 🔄 Daily Workflow (AI Session)

### Start of Session
```
✓ Read .ai/RULES.md (refresh)
✓ Check .ai/MASTER_PROGRESS.md (current status)
✓ Review .ai/MEMORY.md (last decisions)
✓ Open current task from .ai/phases/phase-XX/tasks/TASK_XXX.md
✓ Announce status to user
```

### During Work
```
✓ Implement task according to plan
✓ Log decisions in .ai/MEMORY.md as made
✓ Create/update tests in .ai/planning/ if needed
✓ Update current task file (.ai/phases/.../tasks/...)
```

### End of Session
```
✓ Update task file (mark In Progress/Testing/Completed)
✓ Update .ai/phases/phase-XX/PHASE_STATUS.md
✓ Update .ai/MASTER_PROGRESS.md
✓ Update .ai/MEMORY.md (if decisions made)
✓ Summarize progress to user
```

---

## 📋 File Update Priority

### After EVERY Task (In This Order)
```
1. Task file: .ai/phases/phase-XX/tasks/TASK_XXX.md
   └─ Mark status, add completion date, log effort

2. Phase status: .ai/phases/phase-XX/PHASE_STATUS.md
   └─ Update task counts, progress %, blockers

3. Master progress: .ai/MASTER_PROGRESS.md
   └─ Recalculate overall %, update current task

4. Memory: .ai/MEMORY.md
   └─ Log any decisions or issues encountered

5. Other files: As needed
   └─ TECH_STACK, DATABASE_SCHEMA, API_DESIGN if changed
```

---

## 🎯 Framework at a Glance

**What It Does:**
- Maintains context across AI sessions
- Breaks projects into phases & tasks
- Tracks progress & decisions
- Documents everything systematically
- Enables multiple AI assistants to work on same project

**Key Principles:**
- Small, testable tasks (2-8 hours each)
- Document-driven development
- Context preserved in files
- Decisions logged immediately
- Progress tracked in detail

**Main Artifacts:**
- Project definition → `PROJECT_CONTEXT.md`
- Requirements → `MAIN_REQUIREMENTS.md`
- Architecture → `.ai/planning/` (4 files)
- Phases → `.ai/phases/phase-XX/` (many)
- Tasks → `.ai/phases/phase-XX/tasks/TASK_XXX.md` (many)
- Decisions → `.ai/MEMORY.md` (growing)
- Progress → `.ai/MASTER_PROGRESS.md` (growing)

---

## 💡 Pro Tips

✅ **Always update MEMORY.md** → Decisions are the glue
✅ **Keep MASTER_PROGRESS.md current** → Single source of truth
✅ **Copy templates, don't create from scratch** → Saves time
✅ **Review MEMORY.md at session start** → Maintains context
✅ **Log issues immediately** → Prevents forgotten problems
✅ **Test before marking complete** → Ensures quality
✅ **Customize templates to fit your project** → Make it your own
✅ **Commit files regularly** → Version control your framework

---

## 🔍 Find Things By Purpose

**"I need to see overall progress"**
→ `.ai/MASTER_PROGRESS.md`

**"What was the last decision made?"**
→ `.ai/MEMORY.md` (newest entries)

**"What's the current task?"**
→ `.ai/MASTER_PROGRESS.md` → Current Task section

**"What does this project do?"**
→ `.ai/PROJECT_CONTEXT.md`

**"What technologies are we using?"**
→ `.ai/planning/TECH_STACK.md`

**"What's the database structure?"**
→ `.ai/planning/DATABASE_SCHEMA.md`

**"What are the API endpoints?"**
→ `.ai/planning/API_DESIGN.md`

**"How does the system work?"**
→ `.ai/planning/ARCHITECTURE.md`

**"What are we building?"**
→ `.ai/requirements/MAIN_REQUIREMENTS.md`

**"How do I create a task?"**
→ Copy `.ai/templates/TASK_TEMPLATE.md`

**"I'm an AI starting a new session"**
→ Read `.ai/RULES.md`

---

## 🚀 Getting Started Checklist

- [ ] Opened `README_FRAMEWORK_INDEX.md`
- [ ] Opened `FRAMEWORK_SETUP_COMPLETE.md`
- [ ] Customized `.ai/PROJECT_CONTEXT.md`
- [ ] Filled `.ai/requirements/MAIN_REQUIREMENTS.md`
- [ ] Updated `.ai/planning/TECH_STACK.md`
- [ ] Sketched `.ai/planning/ARCHITECTURE.md`
- [ ] Planned `.ai/planning/DATABASE_SCHEMA.md`
- [ ] Defined `.ai/planning/API_DESIGN.md`
- [ ] Updated `.ai/MASTER_PROGRESS.md` with phases
- [ ] Created first phase folder: `.ai/phases/phase-01-name/`
- [ ] Ready to begin with AI agent!

---

## 📞 Common Questions

**Q: Where do I start?**
A: `README_FRAMEWORK_INDEX.md` (navigation)

**Q: How long does setup take?**
A: 30-60 minutes for project customization

**Q: Can AI pick up where another AI left off?**
A: Yes! All context is preserved in files

**Q: What if I don't know what to write?**
A: Templates have examples and explanations

**Q: How do I track my progress?**
A: Update `.ai/MASTER_PROGRESS.md` after each task

**Q: Where do I put my code?**
A: In `src/` folder, organize by module/feature

**Q: How do I run tests?**
A: Add tests to `tests/` folder, document in test plan

**Q: Can I customize this framework?**
A: Yes! Modify any template to fit your needs

**Q: Does this work with all AI assistants?**
A: Yes! Works with Copilot, Claude, ChatGPT, Gemini, etc.

**Q: What if I lose my way?**
A: Read `.ai/MEMORY.md` and `.ai/MASTER_PROGRESS.md`

---

## ⏱️ Time Estimates

| Activity | Time | When |
|----------|------|------|
| Read framework docs | 15 min | Once |
| Customize for project | 30 min | Once |
| Plan project phases | 60 min | Once |
| Create each phase | 30 min | Per phase |
| Create each task | 5 min | Per task |
| Work on task | 2-8 hrs | Per task |
| Update files | 10 min | After task |
| **Setup to ready** | **~2 hours** | First time |

---

## 🎓 Learning Curve

**First Session:** 30-60 min (setup + customization)
**Second Session:** 10-15 min (mostly working, less setup)
**Ongoing:** 5-10 min (review status, work on task)

---

## 💾 What to Backup

Most important files (in order):
1. `.ai/MEMORY.md` ← All decisions
2. `.ai/MASTER_PROGRESS.md` ← Progress
3. `.ai/PROJECT_CONTEXT.md` ← Project config
4. `.ai/phases/*/tasks/*.md` ← Completed tasks
5. `.ai/planning/` ← All architecture

---

## ✨ Framework Superpowers

🔹 **Context Never Lost** - Files maintain all context
🔹 **Multiple Sessions** - Different AI can continue work
🔹 **Tracks Everything** - Progress, decisions, issues
🔹 **Self-Documenting** - Code is documented as built
🔹 **Systematic** - Never forget what to do next
🔹 **Scalable** - Works for projects of any size
🔹 **Flexible** - Customize to your needs
🔹 **Universal** - Works with any tech stack

---

## 🎯 Your Next Action

**Right Now:**
```
1. Open: README_FRAMEWORK_INDEX.md
2. Read: First 2 sections
3. Decide: Start setup or explore more?
```

**In 10 Minutes:**
You'll understand the complete structure

**In 30 Minutes:**
You'll have customized for your project

**In 1 Hour:**
You'll be ready to work with AI

---

**Framework Version:** 1.0 | **Status:** ✅ Complete | **Date:** Nov 26, 2025

**You're all set! 🚀 Start with README_FRAMEWORK_INDEX.md**
