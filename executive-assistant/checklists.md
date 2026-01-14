# Checklists

Scenario-specific checklists for common situations. Copy and use as needed.

---

## Daily Operations

### Morning Startup
- [ ] Check calendar for today's events
- [ ] Review daily tasks file
- [ ] Process overnight emails/messages
- [ ] Identify top 3 priorities for today
- [ ] Block focus time if needed
- [ ] Prep for any meetings in first half of day

### End of Day Shutdown
- [ ] Review what got done
- [ ] Update task list (complete/defer items)
- [ ] Process inbox to zero (or close)
- [ ] Check tomorrow's calendar
- [ ] Set top 3 priorities for tomorrow
- [ ] Close work apps / set boundaries

---

## Weekly Operations

### Weekly Review (Friday)
- [ ] Process all inboxes to zero
- [ ] Review calendar for next 2 weeks
- [ ] Update all project statuses
- [ ] Identify stalled items
- [ ] Review weekly report
- [ ] Plan next week's priorities
- [ ] Clear completed tasks from Taskwarrior
- [ ] Capture any loose threads
- [ ] Sync calendar: `vdirsyncer sync`

### Week Planning (Monday)
- [ ] Review weekly goals
- [ ] Check key deadlines this week
- [ ] Identify must-do items
- [ ] Block focus time
- [ ] Schedule any needed meetings
- [ ] Review project boards

---

## Monthly Operations

### Monthly Admin
- [ ] Review and send invoices
- [ ] Check accounts receivable (unpaid invoices)
- [ ] Update expense tracking
- [ ] Review recurring subscriptions
- [ ] Back up important files
- [ ] Clean up downloads/desktop
- [ ] Review goals and progress
- [ ] Update contact list with new connections

### End of Month Close
- [ ] Final invoice submissions
- [ ] Expense report if applicable
- [ ] Time tracking reconciliation
- [ ] Update project financials
- [ ] Monthly summary/report

---

## Quarterly Operations

### Quarterly Review
- [ ] Review quarterly goals - what was accomplished?
- [ ] Financial review - revenue, expenses, runway
- [ ] Contract review - renewals, renegotiations
- [ ] Rate review - adjust pricing if needed
- [ ] Tool/subscription audit - what's used, what's not
- [ ] Network review - key relationships to nurture
- [ ] Professional development - courses, conferences
- [ ] Set next quarter goals

### Tax Prep (Quarterly Estimated)
- [ ] Gather income records
- [ ] Categorize expenses
- [ ] Calculate estimated tax
- [ ] Make payment by deadline
- [ ] File any required forms
- [ ] Update tax tracking spreadsheet

---

## Conference Travel

### Pre-Conference (2 weeks before)
- [ ] Confirm registration
- [ ] Book flights
- [ ] Book accommodation
- [ ] Arrange ground transportation
- [ ] Check visa/ID requirements if international
- [ ] Review agenda/schedule
- [ ] Identify key sessions to attend
- [ ] Schedule meetings with contacts attending
- [ ] Prepare business cards if using
- [ ] Update speaker materials if presenting

### Packing - Tech
- [ ] Laptop + charger
- [ ] Phone + charger
- [ ] Portable battery pack
- [ ] Cables (USB-C, Lightning, etc.)
- [ ] Headphones
- [ ] Adapters (power/video if needed)
- [ ] Backup of important files
- [ ] Conference app installed

### Packing - Presentation (if speaking)
- [ ] Slides on laptop
- [ ] Slides on USB backup
- [ ] Slides accessible online (backup)
- [ ] Presenter remote/clicker
- [ ] Dongle for projector connection
- [ ] Demo environment tested
- [ ] Speaker notes printed

### Packing - Documents
- [ ] ID / Passport
- [ ] Conference ticket/badge
- [ ] Travel itinerary printed
- [ ] Hotel confirmation
- [ ] Insurance info if applicable
- [ ] Emergency contacts

### Packing - Personal
- [ ] Clothes for each day + 1 extra
- [ ] Toiletries
- [ ] Medications
- [ ] Snacks
- [ ] Water bottle
- [ ] Notebook/pen
- [ ] Comfortable shoes (conferences = walking)

### At Conference
- [ ] Pick up badge
- [ ] Orient to venue layout
- [ ] Identify quiet work spots
- [ ] Connect with planned meetings
- [ ] Take notes from sessions
- [ ] Collect contact info from new connections
- [ ] Post key insights (Nostr, Twitter)
- [ ] Document for recap content
- [ ] Stay hydrated / take breaks

### Post-Conference (within 48 hours)
- [ ] Follow up with new contacts
- [ ] Send thank-yous as appropriate
- [ ] Process notes into action items
- [ ] Add new contacts to system
- [ ] Write recap post/content
- [ ] Submit expense report
- [ ] Share key learnings with team
- [ ] Thank organizers publicly

---

## Client/Project Onboarding

### New Client Checklist
- [ ] Scope of work documented and agreed
- [ ] Contract signed by both parties
- [ ] Payment terms clear
- [ ] Timeline agreed
- [ ] Communication preferences set
- [ ] Primary contacts identified
- [ ] Project folder created
- [ ] Access/credentials received
- [ ] Kickoff meeting scheduled
- [ ] First invoice terms clear

### Project Kickoff
- [ ] Review SOW with all stakeholders
- [ ] Confirm goals and success criteria
- [ ] Identify dependencies and risks
- [ ] Set communication cadence
- [ ] Create project task list
- [ ] Set up tracking/board if needed
- [ ] Share working document access
- [ ] Schedule first check-in

---

## Project Completion

### Project Closeout
- [ ] All deliverables submitted
- [ ] Client acceptance received
- [ ] Final invoice sent
- [ ] Documentation handed over
- [ ] Access/credentials returned or transferred
- [ ] Project folder organized
- [ ] Lessons learned captured
- [ ] Thank you sent to client
- [ ] Case study potential noted
- [ ] Testimonial requested if appropriate

---

## Meeting Prep

### Before Any Meeting
- [ ] Purpose clear - why are we meeting?
- [ ] Agenda prepared or reviewed
- [ ] Materials/docs ready
- [ ] Questions prepared
- [ ] Calendar invite confirmed
- [ ] Link/location confirmed
- [ ] Tech tested (video, audio, screen share)

### Before Important Meeting
All of above, plus:
- [ ] Research attendees if new
- [ ] Review any previous meeting notes
- [ ] Prepare talking points
- [ ] Anticipate questions/objections
- [ ] Define desired outcome
- [ ] Prep any demos if applicable

### After Any Meeting
- [ ] Capture notes (or clean up live notes)
- [ ] Extract action items
- [ ] Add tasks to Taskwarrior
- [ ] Send follow-up email if needed
- [ ] Schedule any follow-up meetings
- [ ] Update project status if applicable

---

## Content Publishing

### Before Publishing
- [ ] Content reviewed for accuracy
- [ ] Links tested
- [ ] Images/media included and working
- [ ] SEO basics (title, meta, headers)
- [ ] Grammar/spelling check
- [ ] Sensitive info removed
- [ ] Proper attribution for sources
- [ ] CTA clear

### After Publishing
- [ ] Share on primary channels
- [ ] Cross-post as appropriate
- [ ] Notify relevant stakeholders
- [ ] Monitor initial engagement
- [ ] Respond to early comments
- [ ] Note performance for future

---

## Emergency/Backup

### If Laptop Dies
- [ ] Access email via phone/web
- [ ] Access calendar via phone
- [ ] Access critical docs via cloud
- [ ] Contact key people about delay
- [ ] Find replacement device options
- [ ] Restore from backup when recovered

### If Internet Goes Down
- [ ] Mobile hotspot as backup
- [ ] Identify nearby locations with WiFi
- [ ] Prioritize urgent communications
- [ ] Work on offline tasks
- [ ] Communicate delays to affected parties

### If You Get Sick
- [ ] Notify affected parties ASAP
- [ ] Reschedule critical meetings
- [ ] Delegate if possible
- [ ] Set OOO if extended
- [ ] Document status for handoff
- [ ] Don't push through - rest

---

## Tool Sync Issues

### If Taskwarrior Not Syncing
```bash
# Check sync status
task sync

# Force full sync
task sync init

# Check for conflicts
task sync
```

### If Calendar Not Syncing
```bash
# Sync calendars
vdirsyncer sync

# Check for errors
vdirsyncer discover

# Repair if needed
vdirsyncer repair
```

### If Daily Tasks File Missing
```bash
# Run manual sync
cd /home/raven/Projects/devRel
python3 daily_sync.py --sync-to-taskwarrior

# Check output location
ls -la /home/raven/Vault/Soapbox/Work/Tasks/
```

---

_Use these checklists as starting points. Customize for your specific situations._
