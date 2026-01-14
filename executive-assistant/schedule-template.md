# Daily Schedule Template

Generic time-block template for building daily schedules. Customize the blocks and tasks for your role.

---

## DevRel Daily Time Blocks

| Time | Block | Focus | Task Types |
|------|-------|-------|------------|
| 8:00-10:00 | Community Engagement | Presence & trust building | Social platforms, Q&A, onboarding |
| 10:00-12:00 | Code Review & Triage | Stay on top of codebase | PRs, issues, NIPs, testing |
| 12:00-13:00 | Lunch & Async | Recharge | Email, calendar, light reading |
| 13:00-15:30 | Development & Projects | Deep work | Building, shipping, coding |
| 15:30-17:00 | Content Creation | Turn discoveries into content | Tutorials, docs, videos, posts |
| 17:00-18:00 | Events & Planning | Build the future | Conferences, talks, community |
| 18:00-18:30 | End of Day Wrap-up | Close intentionally | Review, tomorrow's priorities |

---

## Weekly Focus Days

| Day | Primary Focus | Why |
|-----|---------------|-----|
| **Monday** | Week planning | Review metrics, set goals, organize week |
| **Tuesday** | Deep dev work | Minimize meetings, maximize building |
| **Wednesday** | Content creation | Publish blog/video, writing focus |
| **Thursday** | Community engagement | Calls, AMAs, live sessions |
| **Friday** | Week review | Documentation cleanup, prep for next week |

---

## Daily Schedule Output Format

Use this format when creating daily schedules:

```markdown
# DAILY SCHEDULE — [Day], [Full Date]

**Focus:** [Weekly Focus for this day]

**Tasks:** [[YYYY-MM-DD-tasks]]

---

### COMPLETED BLOCKS
[List any completed time blocks with checkmarks]

### [EMOJI] [TIME] — [BLOCK NAME] (NOW)
**Current Focus:** [What to work on now]

**Priority Tasks:**
- [ ] Task 1 (priority/due info)
- [ ] Task 2
- [ ] Task 3

### [EMOJI] [TIME] — [BLOCK NAME]
**Tasks:**
- [ ] Task 1
- [ ] Task 2

[... continue for remaining blocks ...]

### EVENING COMMITMENTS
| Time | Event |
|------|-------|
| HH:MM | Event name |
```

---

## Block Emojis

| Block | Emoji | Alt |
|-------|-------|-----|
| Community | | (Community) |
| Code Review | | (Review) |
| Lunch | | (Break) |
| Development | | (Dev) |
| Content | | (Content) |
| Events | | (Events) |
| Wrap-up | | (EOD) |
| Evening | | (Home) |
| Completed | | (Done) |

---

## Task Assignment Rules

When placing tasks in time blocks:

1. **Match task type to block:**
   - Code/PR work → Development block
   - Writing/docs → Content Creation block
   - Conference/travel → Event Planning block
   - Community questions → Community Engagement block

2. **Prioritize by:**
   - Due date (soonest first)
   - Priority level (H > M > L)
   - Blocking items (failed builds, MRs needing action)
   - Time-sensitive items (releases, meetings)

3. **Respect daily focus:**
   - Tuesday = minimize meetings, deep work
   - Wednesday = content creation priority
   - Thursday = community engagement priority

4. **Layer calendar events:**
   - Meetings override the default block
   - Mark meeting time as occupied
   - Distribute remaining tasks around meetings

---

## Building a Schedule: Step by Step

1. **Read today's tasks** from task file
2. **Check calendar** with `khal list today`
3. **Identify current time** and which block we're in
4. **Mark completed blocks** as done
5. **Place calendar events** into the schedule
6. **Assign tasks to blocks** by type and priority
7. **Note evening commitments**
8. **Save to** `/home/raven/Vault/Soapbox/Work/Schedule/YYYY-MM-DD-schedule.md`

---

## Customizing for Other Roles

This template is designed for DevRel. To customize:

1. **Rename blocks** to match your work patterns
2. **Adjust times** to your natural energy rhythms
3. **Change weekly focuses** to match your role cadence
4. **Update task types** for each block

### Example: Engineering Focus

| Time | Block | Focus |
|------|-------|-------|
| 8:00-9:00 | Planning | Daily standup, review PRs |
| 9:00-12:00 | Deep Work | Coding, no meetings |
| 12:00-13:00 | Lunch | Break |
| 13:00-15:00 | Collaboration | Pair programming, meetings |
| 15:00-17:00 | Deep Work | Continue coding |
| 17:00-17:30 | Wrap-up | Commit, update tickets |

### Example: Management Focus

| Time | Block | Focus |
|------|-------|-------|
| 8:00-9:00 | Email & Planning | Triage, priorities |
| 9:00-12:00 | Meetings | 1:1s, team syncs |
| 12:00-13:00 | Lunch | Break |
| 13:00-15:00 | Strategic Work | Planning, documents |
| 15:00-17:00 | Meetings | Cross-team, external |
| 17:00-18:00 | Admin & EOD | Approvals, follow-ups |

---

## Live Document Location

Your live DevRel schedule template with project-specific content:
`/home/raven/Vault/Soapbox/Work/daily-task-schedule.md`

This skill file provides the generic structure. Your Vault file has the current projects, milestones, and specific checklists.

---

_Adapt this template to your work style and role._
