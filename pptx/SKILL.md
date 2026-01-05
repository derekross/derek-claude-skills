---
name: Presentation Creator
description: Create professional PowerPoint presentations for conferences, demos, and talks. Use for Bitcoin/Nostr events, product showcases, and speaker decks.
dependencies: python-pptx>=0.6.21
---

# Presentation Creator

Create polished, professional PowerPoint presentations optimized for technical conferences, product demos, and developer-focused talks.

## When to Use This Skill

Use this skill when you need to:
- Create conference presentation decks
- Build product demo slides
- Prepare speaker materials for events
- Design pitch decks for partnerships or sponsors
- Create educational/onboarding presentations

## Presentation Principles

### Structure
1. **Opening Hook** - Start with a compelling problem or vision (1-2 slides)
2. **Context** - Set the stage, why this matters now (2-3 slides)
3. **Core Content** - Main points, demos, technical details (varies)
4. **Call to Action** - What you want the audience to do (1-2 slides)
5. **Resources** - Links, QR codes, contact info (1 slide)

### Design Guidelines
- **One idea per slide** - Don't overload
- **Large fonts** - Minimum 24pt for body, 36pt+ for headers
- **High contrast** - Ensure readability in any lighting
- **Minimal text** - Use speaker notes for details
- **Consistent branding** - Match event or company colors

### Technical Presentations
For developer/technical audiences:
- Include code snippets (syntax highlighted)
- Use diagrams over bullet points
- Show architecture flows
- Include live demo markers
- Add terminal/CLI screenshots where relevant

## Slide Templates

### Title Slide
- Event name and date
- Talk title (short, memorable)
- Speaker name and handle
- Company/project logo

### Problem/Solution Slide
- Problem statement (1-2 sentences)
- Visual representation of pain point
- Transition to solution

### Demo Slide
- "DEMO" marker clearly visible
- Key points to highlight
- Fallback screenshots if demo fails

### Code Slide
- Minimal, focused code (10-15 lines max)
- Syntax highlighting
- Arrow/highlight for key lines
- Font: monospace, 18pt minimum

### Architecture Slide
- Clean diagram (boxes and arrows)
- Label all components
- Show data flow direction
- Limit to 5-7 components

### CTA Slide
- Single clear action
- QR code for links
- Social handles
- Website URL

## File Output

Generate .pptx files using python-pptx with:
- 16:9 aspect ratio (standard for modern projectors)
- Embedded fonts when possible
- High-resolution images (1920x1080 minimum)
- Speaker notes in Notes section

## Example Prompts This Skill Handles

- "Create a 10-slide presentation for my BTC++ talk on Nostr"
- "Build a demo deck for Shakespeare website builder"
- "Make conference slides about decentralized identity"
- "Create a sponsor pitch deck for NosVegas event"
