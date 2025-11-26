# AI-Driven Development Framework

A universal, reusable framework for AI-assisted software development that maintains context, tracks progress, and ensures systematic implementation across multiple chat sessions with any AI assistant.

## 🎯 Overview

This framework solves the core challenge of AI-assisted development: **losing context between sessions**. Every decision, every progress update, and every technical choice is preserved in well-organized markdown files that any AI can read and understand.

### ✨ Key Features

- 🔄 **Context Persistence** - Never lose project context between AI sessions
- 🤖 **Universal** - Works with GitHub Copilot, Claude, ChatGPT, Gemini, or any AI
- 📊 **Progress Tracking** - Real-time metrics and status updates
- 📝 **Self-Documenting** - Everything is documented as you build
- 📁 **Organized Structure** - Clear separation of concerns and responsibilities
- 🎯 **Systematic Planning** - Break projects into manageable phases and tasks
- ✅ **Quality Assurance** - Built-in testing and validation workflows
- 📚 **Reusable Templates** - Copy and customize for quick setup

## 🚀 Quick Start

### 1. First Time? Start Here
Read these files in order:
1. `README_FRAMEWORK_INDEX.md` - File index and navigation
2. `FRAMEWORK_SETUP_COMPLETE.md` - Setup instructions
3. `QUICK_REFERENCE_CARD.md` - Quick reference

### 2. Customize Your Project (30 minutes)
1. Edit `.ai/PROJECT_CONTEXT.md` - Add your project details
2. Fill `.ai/requirements/MAIN_REQUIREMENTS.md` - Document requirements
3. Update `.ai/planning/TECH_STACK.md` - List your technologies

### 3. Plan Your Phases (1-2 hours)
1. Update `.ai/MASTER_PROGRESS.md` - List your phases
2. Create `.ai/requirements/phases/PHASE_01_[Name].md` - Phase requirements
3. Sketch `.ai/planning/` files - Architecture, database, API

### 4. Start Development
1. Create phase folders in `.ai/phases/phase-01-name/`
2. Copy templates to create tasks
3. Have AI read `.ai/RULES.md` first
4. Begin with Phase 1, Task 1

## 📁 Directory Structure

```
.
├── README.md                           # This file
├── README_FRAMEWORK_INDEX.md           # Complete file index
├── FRAMEWORK_SETUP_COMPLETE.md         # Setup guide
├── QUICK_REFERENCE_CARD.md             # Quick reference
├── COMPLETION_SUMMARY.md               # What was created
│
├── .ai/                                # AI Framework & Planning
│   ├── 00_START_HERE.md               # AI quick start
│   ├── RULES.md                       # Universal framework rules
│   ├── PROJECT_CONTEXT.md             # Project information
│   ├── MEMORY.md                      # Decisions & learnings
│   ├── MASTER_PROGRESS.md             # Overall progress
│   ├── QUICK_START_INSTRUCTIONS.md    # Agent quick guide
│   │
│   ├── requirements/
│   │   ├── MAIN_REQUIREMENTS.md       # Full requirements
│   │   └── phases/                    # Phase requirements
│   │
│   ├── planning/
│   │   ├── TECH_STACK.md              # Technologies
│   │   ├── ARCHITECTURE.md            # System design
│   │   ├── DATABASE_SCHEMA.md         # Database structure
│   │   └── API_DESIGN.md              # API specifications
│   │
│   ├── templates/
│   │   ├── TASK_TEMPLATE.md           # Task template
│   │   ├── PHASE_TEMPLATE.md          # Phase template
│   │   ├── TEST_PLAN_TEMPLATE.md      # Test plan template
│   │   └── IMPLEMENTATION_PLAN_TEMPLATE.md
│   │
│   └── phases/                         # Phase folders (create per phase)
│       └── phase-01-[name]/
│           ├── PHASE_STATUS.md
│           ├── IMPLEMENTATION_PLAN.md
│           ├── tasks/
│           │   ├── TASK_001_[Name].md
│           │   ├── TASK_002_[Name].md
│           │   └── ...
│           └── testing/
│               ├── TEST_PLAN.md
│               └── TEST_RESULTS.md
│
├── src/                                # Source code
├── tests/                              # Test files
└── docs/                               # Documentation
```

## 📋 Core Files Overview

### Essential Framework Files
- **`00_START_HERE.md`** - AI quick start reference (read every session)
- **`RULES.md`** - Framework rules and workflow (comprehensive guide)
- **`PROJECT_CONTEXT.md`** - Project information template
- **`MASTER_PROGRESS.md`** - Overall project progress tracking
- **`MEMORY.md`** - Technical decisions and learnings
- **`QUICK_START_INSTRUCTIONS.md`** - Quick reference for agents

### Planning & Design
- **`TECH_STACK.md`** - Document technology choices
- **`ARCHITECTURE.md`** - System architecture and design
- **`DATABASE_SCHEMA.md`** - Database structure and relationships
- **`API_DESIGN.md`** - API endpoints and specifications

### Requirements
- **`MAIN_REQUIREMENTS.md`** - Complete project requirements

### Templates (Copy to create new items)
- **`TASK_TEMPLATE.md`** - Copy for each task
- **`PHASE_TEMPLATE.md`** - Copy for each phase
- **`TEST_PLAN_TEMPLATE.md`** - Copy for tests
- **`IMPLEMENTATION_PLAN_TEMPLATE.md`** - Copy for phase planning

## 🔄 Daily Workflow

### Start of Each AI Session
```
1. Read .ai/00_START_HERE.md
2. Read .ai/RULES.md (refresh)
3. Check .ai/MASTER_PROGRESS.md (current status)
4. Review .ai/MEMORY.md (recent entries)
5. Open current task
```

### During Work
```
1. Implement according to plan
2. Log decisions in .ai/MEMORY.md
3. Update task file with progress
4. Create/update tests
```

### End of Session
```
1. Update task file (status, effort, notes)
2. Update .ai/phases/phase-XX/PHASE_STATUS.md
3. Update .ai/MASTER_PROGRESS.md
4. Update .ai/MEMORY.md (if decisions made)
5. Summarize progress to user
```

## 💡 Key Principles

### Context Persistence Over Intelligence
The framework works because context is preserved in files, not because of AI capability.

### Small Steps, Validated
Each task is small (2-8 hours), tested, and validated before moving forward.

### Documentation Is Development
Files aren't overhead—they ARE the development process.

### Systematic Over Chaotic
Follow the rules systematically, and progress happens steadily.

## 🎯 File Update Checklist

After **every task**, update (in this order):
- [ ] Task file (`.ai/phases/phase-XX/tasks/TASK_XXX.md`)
- [ ] Phase status (`.ai/phases/phase-XX/PHASE_STATUS.md`)
- [ ] Master progress (`.ai/MASTER_PROGRESS.md`)
- [ ] Memory (`.ai/MEMORY.md` - if applicable)

## 📊 Statistics

| Metric | Value |
|--------|-------|
| Total Files | 18 |
| Core Framework | 6 files |
| Planning & Design | 4 files |
| Templates | 4 files |
| Navigation Guides | 3 files |
| Total Lines | ~6,500+ |
| Typical Setup Time | 30-60 minutes |

## 🤖 Using with AI Assistants

### First Time with an AI
1. Share `.ai/RULES.md` - Framework rules
2. Share `.ai/PROJECT_CONTEXT.md` - Project info
3. Share `.ai/requirements/MAIN_REQUIREMENTS.md` - Requirements
4. Command: "Start with Phase 1, Task 1"

### Returning to Project with Different AI
1. Have new AI read `.ai/RULES.md`
2. Have new AI read `.ai/MEMORY.md` (recent entries)
3. Have new AI read `.ai/MASTER_PROGRESS.md`
4. Open current task file
5. Continue work

## ✅ Verification Checklist

Verify framework is complete:
- [ ] `.ai/` folder with 6 core files
- [ ] `.ai/planning/` with 4 files
- [ ] `.ai/requirements/` with requirements file
- [ ] `.ai/templates/` with 4 templates
- [ ] `src/`, `tests/`, `docs/` directories
- [ ] All guide files in root
- [ ] Ready to customize

## 🎓 Learning Path

### Beginner (15 minutes)
1. Read `README_FRAMEWORK_INDEX.md`
2. Skim `FRAMEWORK_SETUP_COMPLETE.md`
3. Understand overall structure

### Intermediate (30 minutes)
1. Customize `PROJECT_CONTEXT.md`
2. Fill `MAIN_REQUIREMENTS.md`
3. Start planning phases

### Advanced (1-2 hours)
1. Create phase structure
2. Create tasks using templates
3. Start with AI
4. Learn workflow through practice

## 📚 File Quick Reference

| Need | Go To |
|------|-------|
| Project overview | `.ai/PROJECT_CONTEXT.md` |
| Overall progress | `.ai/MASTER_PROGRESS.md` |
| Past decisions | `.ai/MEMORY.md` |
| Current status | `.ai/MASTER_PROGRESS.md` |
| Current task | `MASTER_PROGRESS.md` → current task |
| How it works | `.ai/RULES.md` |
| Technology stack | `.ai/planning/TECH_STACK.md` |
| Database info | `.ai/planning/DATABASE_SCHEMA.md` |
| API specs | `.ai/planning/API_DESIGN.md` |
| System design | `.ai/planning/ARCHITECTURE.md` |
| Full requirements | `.ai/requirements/MAIN_REQUIREMENTS.md` |
| Phase structure | `.ai/templates/PHASE_TEMPLATE.md` |
| Task structure | `.ai/templates/TASK_TEMPLATE.md` |

## 🚀 Getting Started Right Now

### Step 1 (2 minutes)
Open `README_FRAMEWORK_INDEX.md`

### Step 2 (5 minutes)
Read `FRAMEWORK_SETUP_COMPLETE.md`

### Step 3 (30 minutes)
Customize for your project:
- Edit `.ai/PROJECT_CONTEXT.md`
- Fill `.ai/requirements/MAIN_REQUIREMENTS.md`
- Update `.ai/planning/TECH_STACK.md`

### Step 4 (Ready!)
Begin using with AI assistant

## 💾 Backup Important Files

Most critical (in order):
1. `.ai/MEMORY.md` - All decisions
2. `.ai/MASTER_PROGRESS.md` - Progress
3. `.ai/PROJECT_CONTEXT.md` - Configuration
4. `.ai/phases/*/tasks/*.md` - Completed tasks
5. `.ai/planning/` - Architecture

## 📞 Common Questions

**Q: Where do I start?**
A: Read `README_FRAMEWORK_INDEX.md` for navigation

**Q: Can different AIs work on same project?**
A: Yes! All context is preserved in files

**Q: How long is setup?**
A: 30-60 minutes for project customization

**Q: Does this work with my tech stack?**
A: Yes! Works with any technology

**Q: What if I get stuck?**
A: Read `QUICK_REFERENCE_CARD.md` or `.ai/RULES.md`

**Q: Can I modify the framework?**
A: Yes! Customize any template to fit your needs

## 📝 Next Steps

1. ⭐ **Read:** `README_FRAMEWORK_INDEX.md`
2. 📖 **Understand:** `FRAMEWORK_SETUP_COMPLETE.md`
3. ✏️ **Customize:** `.ai/PROJECT_CONTEXT.md`
4. 📋 **Plan:** `.ai/requirements/MAIN_REQUIREMENTS.md`
5. 🚀 **Start:** With AI using `.ai/RULES.md`

---

## 📄 License

Free to use and modify. This framework is designed to be universal and adaptable to any project.

## 🙋 Support

All documentation is self-contained in this framework. Everything you need is in the `.ai/` folder and guide files.

---

**Framework Version:** 1.0  
**Created:** November 26, 2025  
**Status:** ✅ Ready to Use  
**Compatible:** GitHub Copilot, Claude, ChatGPT, Gemini, any AI assistant

---

**Ready to get started? Open `README_FRAMEWORK_INDEX.md` now! 🎉**
