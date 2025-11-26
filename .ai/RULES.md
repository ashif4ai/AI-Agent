# AI AGENT RULES - UNIVERSAL FRAMEWORK

## 🎯 Core Principle
Maintain perfect context across all chat sessions through systematic file management.

---

## 📖 Session Initialization Protocol

### Every New Session:
1. ✅ Read `.ai/00_START_HERE.md`
2. ✅ Read `.ai/RULES.md` (this file)
3. ✅ Read `.ai/PROJECT_CONTEXT.md`
4. ✅ Read `.ai/MASTER_PROGRESS.md`
5. ✅ Read `.ai/MEMORY.md` (at least recent entries)
6. ✅ Navigate to current phase: `.ai/phases/phase-0X-name/PHASE_STATUS.md`
7. ✅ Open current task: `.ai/phases/phase-0X-name/tasks/TASK_XXX_NAME.md`

### Announce to User:
```
📊 PROJECT STATUS
Project: [Name]
Phase: [X/Y] - [Phase Name]
Task: [XXX] - [Task Name] 
Status: [Current Status]
Progress: [X%]
Last Updated: [Date]

Ready to continue. What would you like to do?
```

---

## 🗂️ File Locations Reference

| File Type | Location | Purpose |
|-----------|----------|---------|
| Requirements | `.ai/requirements/MAIN_REQUIREMENTS.md` | Full project requirements |
| Phase Requirements | `.ai/requirements/phases/PHASE_0X_[NAME].md` | Phase-specific requirements |
| Master Progress | `.ai/MASTER_PROGRESS.md` | Overall project tracking |
| Phase Progress | `.ai/phases/phase-0X-name/PHASE_STATUS.md` | Phase-level tracking |
| Tasks | `.ai/phases/phase-0X-name/tasks/TASK_XXX_NAME.md` | Individual task details |
| Memory | `.ai/MEMORY.md` | Decisions, issues, learnings |
| Tech Stack | `.ai/planning/TECH_STACK.md` | Technology choices |
| Architecture | `.ai/planning/ARCHITECTURE.md` | System design |
| Database | `.ai/planning/DATABASE_SCHEMA.md` | Database structure |
| APIs | `.ai/planning/API_DESIGN.md` | API specifications |

---

## 🔄 Development Workflow

### Phase Management
1. **Phase Creation:**
   - Copy from `.ai/templates/PHASE_TEMPLATE.md`
   - Create folder: `.ai/phases/phase-0X-[name]/`
   - Create required files: PHASE_STATUS.md, IMPLEMENTATION_PLAN.md
   - Create subfolders: `tasks/`, `testing/`

2. **Phase Breakdown:**
   - Divide phase requirements into 5-15 tasks
   - Each task = 2-8 hours of work
   - Tasks must be independently testable
   - Number tasks sequentially: TASK_001, TASK_002...

### Task Management

#### Task Creation:
```markdown
1. Copy from `.ai/templates/TASK_TEMPLATE.md`
2. Name: TASK_XXX_[DESCRIPTIVE_NAME].md
3. Fill all sections
4. Link to phase requirement
5. Define clear acceptance criteria
```

#### Task Lifecycle:
```
Not Started → In Progress → Testing → Completed
```

#### Task Implementation Process:
1. **Start Task:**
   - Update task status to "In Progress"
   - Update PHASE_STATUS.md
   - Update MASTER_PROGRESS.md

2. **Implement:**
   - Write code with comments
   - Follow project patterns
   - Log decisions in MEMORY.md
   - Handle errors properly

3. **Create Tests:**
   - Generate TEST_PLAN.md for task
   - Include manual test steps
   - Define expected results
   - Cover edge cases

4. **Mark for Testing:**
   - Update task status to "Testing"
   - Provide clear test instructions to user
   - Wait for user validation

5. **Complete Task:**
   - User confirms tests pass
   - Update task status to "Completed"
   - Add completion date
   - Update PHASE_STATUS.md (increment completed tasks)
   - Update MASTER_PROGRESS.md (recalculate percentage)
   - Log any learnings in MEMORY.md

---

## 📝 Mandatory File Updates

### After EVERY Task:

| File | What to Update | When |
|------|---------------|------|
| **Task File** | Status, completion date, notes | Always |
| **PHASE_STATUS.md** | Task count, percentage, blockers | Always |
| **MASTER_PROGRESS.md** | Current task, overall %, hours | Always |
| **MEMORY.md** | Decisions, issues, solutions | If applicable |
| **TECH_STACK.md** | New dependencies | If added |
| **DATABASE_SCHEMA.md** | Schema changes | If modified |
| **API_DESIGN.md** | New/changed endpoints | If modified |

### Update Sequence:
```
1. Task file (mark completed)
2. PHASE_STATUS.md (update counts)
3. MASTER_PROGRESS.md (recalculate)
4. MEMORY.md (log learnings)
5. Other files (as needed)
```

---

## 🧠 Memory Management

### Always Log in MEMORY.md:

#### Technical Decisions
```markdown
| Date | Decision | Rationale | Impact |
```

#### Issues & Solutions
```markdown
| Date | Issue | Solution | Files Affected |
```

#### Dependencies
```markdown
| Date | Package | Version | Purpose |
```

#### Database Changes
```markdown
| Date | Table | Change | Migration |
```

#### API Changes
```markdown
| Date | Endpoint | Change Type | Reason |
```

---

## 🧪 Testing Requirements

### When to Generate Tests:
- After each task (preferred)
- After group of related tasks (max 3 tasks)
- Before phase completion (comprehensive)
- After bug fixes

### Test Plan Must Include:
1. **Setup:** Prerequisites, test data, environment
2. **Test Cases:** Step-by-step instructions
3. **Expected Results:** What should happen
4. **Edge Cases:** Boundary conditions, errors
5. **Acceptance Criteria:** Pass/fail criteria

### Test Validation:
- User must manually test
- User must confirm results
- Only then mark task as "Completed"

---

## 💡 Code Standards

### General:
- Clean, readable code
- Meaningful variable/function names
- Comments for complex logic
- Consistent formatting
- DRY principle (Don't Repeat Yourself)

### Security:
- Never hardcode credentials
- Validate all inputs
- Sanitize user data
- Use environment variables
- Implement proper auth/authz

### Error Handling:
- Try-catch blocks
- Meaningful error messages
- Log errors
- Graceful degradation
- User-friendly messages

---

## 🚨 Error Recovery Protocol

### When Error Occurs:
1. **Immediate:**
   - Log in MEMORY.md with timestamp
   - Mark task as "Blocked" if can't proceed
   - Update PHASE_STATUS.md with blocker

2. **Analysis:**
   - Document error details
   - Identify root cause
   - Research solutions

3. **Resolution:**
   - Propose solution to user
   - Get approval if major change
   - Implement fix
   - Update MEMORY.md with outcome
   - Remove blocker status

4. **Prevention:**
   - Document lesson learned
   - Update implementation approach
   - Add to test cases

---

## 📊 Progress Calculation

### Task Progress:
```
Phase % = (Completed Tasks / Total Tasks) × 100
```

### Overall Progress:
```
Project % = (Σ Phase % × Phase Weight) / 100
```

### Time Tracking:
- Log hours spent per task
- Compare vs. estimate
- Update MASTER_PROGRESS.md

---

## 🗣️ Communication Rules

### Session Start:
- Always announce current status
- Summarize last session's work
- Identify next steps

### During Work:
- Explain what you're doing
- Ask for clarification when needed
- Propose solutions before major changes
- Report blockers immediately

### Session End:
- Summarize what was completed
- List what's next
- Highlight any blockers
- Confirm all files updated

---

## ✅ Completion Criteria

### Task is Complete When:
- [ ] Code implemented and working
- [ ] Test plan created
- [ ] User validated tests
- [ ] Task file updated (status = Completed, date filled)
- [ ] PHASE_STATUS.md updated
- [ ] MASTER_PROGRESS.md updated
- [ ] MEMORY.md updated (if needed)

### Phase is Complete When:
- [ ] All tasks completed
- [ ] All tests passed
- [ ] Phase documentation complete
- [ ] PHASE_STATUS.md shows 100%
- [ ] MASTER_PROGRESS.md updated
- [ ] Ready to move to next phase

### Project is Complete When:
- [ ] All phases completed
- [ ] All requirements met
- [ ] All tests passed
- [ ] Documentation complete
- [ ] Deployment successful
- [ ] User acceptance obtained

---

## 🔧 Technology Stack Rules

### Before Adding Tech:
1. Check if already in TECH_STACK.md
2. If not, ask user for approval
3. Document rationale
4. Update TECH_STACK.md
5. Log in MEMORY.md

### Consistency:
- Use approved tech only
- Follow established patterns
- Don't mix competing solutions
- Keep dependencies minimal

---

## 📌 Important Reminders

### DO:
✅ Read initialization files every session
✅ Update files after every task
✅ Log all decisions and issues
✅ Generate test plans
✅ Wait for user validation
✅ Be systematic and thorough

### DON'T:
❌ Skip file updates
❌ Mark tasks complete without testing
❌ Add tech without approval
❌ Make major changes without discussion
❌ Lose context between sessions
❌ Assume previous work without checking

---

## 🎓 Framework Philosophy

**Persistence over Intelligence:**
The framework works because context is preserved, not because of AI capability.

**Small Steps, Validated:**
Each task is small, tested, and validated before moving forward.

**Documentation is Development:**
Files aren't overhead—they ARE the development process.

**Trust the System:**
Follow the rules systematically, and the project will progress steadily.

---

**Framework Version:** 1.0
**Compatible With:** GitHub Copilot, Claude, ChatGPT, Gemini, any AI assistant
**License:** Free to use and modify
