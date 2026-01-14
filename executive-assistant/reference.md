# CLI Quick Reference

Cheatsheet for command-line tools used in daily workflow.

---

## Taskwarrior

### Creating Tasks

```bash
# Basic task
task add "Task description"

# With project
task add "Task description" project:soapbox

# With priority (H/M/L)
task add "Task description" priority:H

# With due date
task add "Task description" due:tomorrow
task add "Task description" due:friday
task add "Task description" due:2026-01-20
task add "Task description" due:eow        # end of week
task add "Task description" due:eom        # end of month

# Combined
task add "Review Shakespeare PR" project:soapbox priority:H due:tomorrow
```

### Viewing Tasks

```bash
# List all pending tasks
task list

# List by project
task project:soapbox list

# List high priority
task priority:H list

# List due today
task due:today list

# List due this week
task due.before:eow list

# List overdue
task +OVERDUE list

# List ready to work on
task +READY list

# View task details
task <id> info
```

### Modifying Tasks

```bash
# Mark complete
task <id> done

# Modify attributes
task <id> modify priority:H
task <id> modify due:friday
task <id> modify project:conferences

# Add annotation
task <id> annotate "Note about this task"

# Start working on task
task <id> start

# Stop working on task
task <id> stop

# Delete task
task <id> delete
```

### GitLab Tasks (Custom Attributes)

```bash
# List all GitLab-synced tasks
task +gitlab list

# List by GitLab project
task gitlab_project:shakespeare list
task gitlab_project.contains:soapbox list

# View GitLab URL
task <id> info | grep gitlab_url
```

### Useful Filters

```bash
# Tasks modified today
task modified:today list

# Tasks completed today
task end:today completed

# Tasks completed this week
task end.after:today-7d completed

# Waiting tasks
task +WAITING list

# Tasks with no project
task project: list
```

### Reports

```bash
# Summary by project
task summary

# History
task history

# Burndown
task burndown.daily
```

---

## khal (Calendar)

### Viewing Calendar

```bash
# Today's events
khal list today

# Today + next 7 days
khal list today 7d

# Specific date
khal list 2026-01-20

# Date range
khal list 2026-01-20 2026-01-25

# This week
khal list today eow

# Interactive calendar view
khal interactive
```

### Creating Events

```bash
# Basic event with time
khal new 2026-01-20 14:00 15:00 "Meeting title"

# With location
khal new 2026-01-20 14:00 15:00 "Meeting title" -l "Conference Room A"

# With description
khal new 2026-01-20 14:00 15:00 "Meeting title" -d "Agenda: discuss Q1 goals"

# All-day event
khal new 2026-01-20 "Conference Day"

# Multi-day event
khal new 2026-01-20 2026-01-22 "Bitcoin Conference 2026"

# Tomorrow at time
khal new tomorrow 10:00 11:00 "Team standup"

# Relative time expressions
khal new "next monday" 09:00 10:00 "Weekly planning"
```

### Event Management

```bash
# Edit event (interactive)
khal edit

# Delete event (interactive)
khal edit  # then select and delete
```

### Sync

```bash
# Sync all calendars
vdirsyncer sync

# Discover new calendars
vdirsyncer discover
```

---

## khard (Contacts)

### Viewing Contacts

```bash
# List all contacts
khard list

# Search by name
khard list john
khard list "john smith"

# Search by company
khard list soapbox

# Show full contact details
khard show "John Smith"
khard show john  # if unique match
```

### Contact Details

```bash
# Get email address
khard show john | grep -i email

# Get phone number
khard show john | grep -i tel

# Export as vCard
khard show john --format vcard
```

### Managing Contacts

```bash
# Add new contact (interactive)
khard new

# Edit contact
khard edit "John Smith"

# Delete contact
khard remove "John Smith"

# Merge duplicates
khard merge "John Smith" "J Smith"
```

### Sync

```bash
# Sync contacts with Google
vdirsyncer sync google_contacts
```

---

## vdirsyncer (Sync)

### Common Commands

```bash
# Sync everything
vdirsyncer sync

# Sync specific collection
vdirsyncer sync google_calendar
vdirsyncer sync google_contacts

# Discover new calendars/address books
vdirsyncer discover

# Repair sync issues
vdirsyncer repair

# Check status
vdirsyncer metasync
```

### Troubleshooting

```bash
# Force full sync
vdirsyncer sync --force-delete

# Debug mode
vdirsyncer -vdebug sync
```

---

## Daily Sync Scripts

Location: `/home/raven/Projects/devRel/`

### Manual Sync

```bash
# Full daily sync (calendar + GitLab + Taskwarrior)
cd /home/raven/Projects/devRel
python3 daily_sync.py --sync-to-taskwarrior

# Dry run (preview without saving)
python3 daily_sync.py --dry-run

# Generate weekly report
python3 weekly_report.py

# Weekly report dry run
python3 weekly_report.py --dry-run
```

### Output Locations

```bash
# Daily tasks file
/home/raven/Vault/Soapbox/Work/Tasks/YYYY-MM-DD-tasks.md

# Daily schedule
/home/raven/Vault/Soapbox/Work/Schedule/YYYY-MM-DD-schedule.md

# Weekly reports
/home/raven/Vault/Soapbox/Work/Tasks/Reports/YYYY-WNN-report.md

# Meeting notes
/home/raven/Vault/Soapbox/Meetings/YYYY-MM-DD-topic.md
```

---

## File Operations

### Quick File Access

```bash
# Today's task file
cat ~/Vault/Soapbox/Work/Tasks/$(date +%Y-%m-%d)-tasks.md

# Today's schedule
cat ~/Vault/Soapbox/Work/Schedule/$(date +%Y-%m-%d)-schedule.md

# Latest weekly report
ls -t ~/Vault/Soapbox/Work/Tasks/Reports/*.md | head -1 | xargs cat
```

### Common Paths

| What | Path |
|------|------|
| Tasks | `~/Vault/Soapbox/Work/Tasks/` |
| Schedules | `~/Vault/Soapbox/Work/Schedule/` |
| Reports | `~/Vault/Soapbox/Work/Tasks/Reports/` |
| Meetings | `~/Vault/Soapbox/Meetings/` |
| DevRel Scripts | `~/Projects/devRel/` |
| Schedule Template | `~/Vault/Soapbox/Work/daily-task-schedule.md` |

---

## Git Quick Reference

### Daily Operations

```bash
# Status
git status

# Stage all changes
git add .

# Stage specific file
git add path/to/file

# Commit with message
git commit -m "message"

# Push to remote
git push

# Pull latest
git pull
```

### Branches

```bash
# List branches
git branch

# Create and switch to new branch
git checkout -b feature-name

# Switch branches
git checkout main

# Delete local branch
git branch -d feature-name
```

---

## Quick Aliases (if configured)

```bash
# Common task aliases
t       # task list
ta      # task add
td      # task done

# Calendar
k       # khal list today 7d
ki      # khal interactive
kn      # khal new

# Sync
sync    # vdirsyncer sync
```

---

## Troubleshooting

### Taskwarrior Issues

```bash
# Reset sync
task sync init

# Check data location
task _show | grep data.location

# Verify configuration
task show
```

### Calendar Issues

```bash
# Check vdirsyncer config
cat ~/.config/vdirsyncer/config

# Test connection
vdirsyncer discover

# Clear and re-sync
vdirsyncer sync --force-delete
```

### Contact Issues

```bash
# Check khard config
cat ~/.config/khard/khard.conf

# Verify address book location
khard show --help
```

---

_Keep this reference handy for quick lookups._
