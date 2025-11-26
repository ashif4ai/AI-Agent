# Quick Start Instructions for AI Agents

## Initial Project Setup

1. **Create Directory Structure:**
   ```bash
   mkdir -p .ai/{requirements/phases,planning,phases,templates}
   mkdir -p src tests docs
   ```

2. **Copy Template Files:**
   - Copy all templates from this framework
   - Customize PROJECT_CONTEXT.md with project details
   - Fill in MAIN_REQUIREMENTS.md
   - Initialize other core files

3. **First Session Checklist:**
   - [ ] All template files in place
   - [ ] PROJECT_CONTEXT.md filled
   - [ ] MAIN_REQUIREMENTS.md complete
   - [ ] RULES.md reviewed
   - [ ] TECH_STACK.md decided
   - [ ] Phases identified
   - [ ] Phase requirements created

## Every Session Checklist

**At Start:**
- [ ] Read 00_START_HERE.md
- [ ] Review RULES.md
- [ ] Check MASTER_PROGRESS.md
- [ ] Review recent MEMORY.md entries
- [ ] Locate current task
- [ ] Announce status to user

**During Work:**
- [ ] Update task status to "In Progress"
- [ ] Implement according to plan
- [ ] Log decisions/issues in MEMORY.md
- [ ] Create/update tests
- [ ] Follow code standards

**At End:**
- [ ] Update task file
- [ ] Update PHASE_STATUS.md
- [ ] Update MASTER_PROGRESS.md
- [ ] Update MEMORY.md
- [ ] Commit all changes
- [ ] Summarize to user

## Common Commands

### Check Status
```bash
# View current progress
cat .ai/MASTER_PROGRESS.md

# View current phase
cat .ai/phases/phase-0X-name/PHASE_STATUS.md

# View current task
cat .ai/phases/phase-0X-name/tasks/TASK_XXX_NAME.md
```

### Update Files
```bash
# Always update these after task completion:
# 1. .ai/phases/phase-0X-name/tasks/TASK_XXX_NAME.md
# 2. .ai/phases/phase-0X-name/PHASE_STATUS.md
# 3. .ai/MASTER_PROGRESS.md
# 4. .ai/MEMORY.md (if applicable)
```

## File Update Templates

### Task Completion Update
```markdown
### [YYYY-MM-DD] - Completed
- Status changed to "Completed"
- Tests validated by: [User name]
- Actual effort: [X hours]
- Notes: [Any final notes]
```

### Memory Log Entry
```markdown
| YYYY-MM-DD | [Decision/Issue] | [Details] | [Impact/Solution] | User/AI |
```

### Progress Update
```markdown
## Recent Activity
### [YYYY-MM-DD] - Session X
- **Tasks Completed:** TASK_XXX
- **Hours:** X
- **Progress:** +Y%
- **Notes:** [Summary]
```

## Troubleshooting

### Lost Context?
1. Read RULES.md
2. Read MASTER_PROGRESS.md
3. Read last 10 entries in MEMORY.md
4. Check current phase PHASE_STATUS.md
5. Review current task file

### Unclear What to Do?
1. Check MASTER_PROGRESS.md for current task
2. Read current task file
3. Review IMPLEMENTATION_PLAN.md for phase
4. Check for blockers in PHASE_STATUS.md

### Files Not Updated?
- This breaks context persistence!
- Go back and update:
  1. Task file
  2. PHASE_STATUS.md
  3. MASTER_PROGRESS.md
  4. MEMORY.md

---

**Framework Complete! 🎉**

**Total Template Files:**
1. 00_START_HERE.md
2. RULES.md
3. PROJECT_CONTEXT.md
4. MEMORY.md
5. MASTER_PROGRESS.md
6. TASK_TEMPLATE.md
7. PHASE_TEMPLATE.md
8. TEST_PLAN_TEMPLATE.md
9. IMPLEMENTATION_PLAN_TEMPLATE.md
10. TECH_STACK.md
11. MAIN_REQUIREMENTS.md
12. QUICK_START_INSTRUCTIONS.md

Plus: DATABASE_SCHEMA.md, API_DESIGN.md, ARCHITECTURE.md, Phase-specific files

---
**Last Updated:** [Auto-update]
