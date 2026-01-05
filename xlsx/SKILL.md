---
name: Spreadsheet Manager
description: Create and edit Excel spreadsheets for budgets, expense tracking, event planning, project management, and data analysis. Use for financial and organizational tasks.
dependencies: openpyxl>=3.1.0, pandas>=2.0.0
---

# Spreadsheet Manager

Create professional Excel spreadsheets for financial tracking, project management, and data organization.

## When to Use This Skill

Use this skill when you need to:
- Track expenses and income (subcontractor finances)
- Create event budgets
- Manage project timelines
- Organize contact lists
- Analyze data and create reports
- Build tracking dashboards
- Plan conference logistics

## Spreadsheet Templates

### Expense Tracker (Subcontractor)
**Columns:**
- Date
- Category (Travel, Software, Equipment, Services, etc.)
- Description
- Vendor/Payee
- Amount
- Payment Method
- Receipt (Y/N)
- Tax Deductible (Y/N)
- Notes

**Features:**
- Monthly subtotals
- Category summaries
- Running total
- Tax-deductible summary

### Invoice Log
**Columns:**
- Invoice #
- Client
- Date Issued
- Due Date
- Amount
- Status (Sent, Paid, Overdue)
- Date Paid
- Payment Method
- Notes

**Features:**
- Overdue highlighting (conditional formatting)
- Monthly revenue totals
- Outstanding balance calculation

### Event Budget
**Sections:**
- Venue & Logistics
- Marketing & Promotion
- Speakers & Talent
- Food & Beverage
- A/V & Equipment
- Swag & Materials
- Contingency (10-15%)

**Columns per item:**
- Line Item
- Estimated Cost
- Actual Cost
- Variance
- Vendor
- Status
- Notes

### Conference Planning Tracker
**Sheets:**
1. **Overview** - Event details, key dates, budget summary
2. **Tasks** - Task, Owner, Due Date, Status, Dependencies
3. **Speakers** - Name, Topic, Status, Travel, Accommodations
4. **Sponsors** - Company, Level, Contact, Amount, Deliverables
5. **Logistics** - Venue, Catering, A/V, Signage, etc.
6. **Attendees** - Registration tracking (if applicable)

### Content Calendar
**Columns:**
- Date
- Platform (Twitter, Blog, Nostr, Reddit, etc.)
- Content Type (Post, Thread, Article, Video)
- Topic
- Status (Idea, Draft, Scheduled, Published)
- Link
- Engagement Notes

## Formulas & Functions

### Common Formulas
```
=SUM(range)           # Totals
=SUMIF(criteria)      # Conditional totals
=IF(condition,true,false)  # Logic
=VLOOKUP(value,table,col,false)  # Lookups
=TODAY()              # Current date
=DATEDIF(start,end,"d")  # Days between dates
```

### Conditional Formatting Rules
- Red: Overdue items, negative variance, unpaid
- Yellow: Due soon (within 7 days)
- Green: Completed, paid, under budget

## Formatting Standards

### Structure
- Header row: Bold, frozen pane
- Alternating row colors for readability
- Currency format for money columns
- Date format: YYYY-MM-DD or MM/DD/YYYY
- Column widths optimized for content

### Sheets Organization
- Summary/Dashboard as first sheet
- Detail sheets follow logically
- Reference data in separate sheets
- Clear sheet naming conventions

## File Output

Generate .xlsx files using openpyxl with:
- Proper data types (numbers, dates, currency)
- Formulas that calculate automatically
- Conditional formatting
- Print area defined
- Filters on header rows

## Example Prompts This Skill Handles

- "Create an expense tracker for my consulting business"
- "Build a budget spreadsheet for NosVegas event"
- "Make a content calendar for Q1 2026"
- "Track my invoices and payments"
- "Create a conference planning spreadsheet for Bitcoin Week"
