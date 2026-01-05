---
name: nostr-devrel-toolkit
description: Developer Relations toolkit for Nostr ecosystem and freedom tech. Use for community building, developer advocacy, conference prep, Shakespeare demos/workshops, and decentralized social evangelism.
---

# Nostr DevRel Toolkit

A comprehensive Developer Relations toolkit for advocating Nostr protocol, freedom tech, and community empowerment. Tailored for Soapbox/AOS work including Shakespeare, community initiatives, and conference activities.

## When to Use This Skill

Use this skill when you need to:
- Create content about Nostr or decentralized social
- Prepare conference talks or demos
- Plan and run Shakespeare workshops
- Onboard new users or developers
- Plan community events (NosVegas, meetups)
- Develop Shakespeare demos and materials
- Write technical documentation
- Engage with the Nostr community
- Support diVine or other product launches

## Core Philosophy

### Own Your Social Life
Nostr empowers communities and individuals to:
- **Own their social content** - Your posts, your data, forever
- **Own their social graph** - Your followers and connections belong to you
- **Own their identity** - Cryptographic keys, not platform accounts
- **Own their reach** - No algorithm deciding who sees your content

### Freedom Tech: Money + Communication
Freedom money (Bitcoin) and freedom communication (Nostr) go hand in hand:
- Censorship-resistant money needs censorship-resistant communication
- Self-sovereign identity extends to both financial and social life
- Open protocols beat closed platforms in both domains
- But lead with the social benefits—the financial benefits follow naturally

### The Relationship-First Approach
**Build relationships → Build trust → Recognition and adoption follow through osmosis**

This means:
- Don't lead with "Bitcoin fixes this"
- Don't be preachy or heavy-handed
- Show genuine interest in what people are building
- Help people solve their actual problems
- Let the technology speak through experience
- People adopt tools they see working for people they trust

### What We're NOT About
- Forcing Bitcoin talking points into every conversation
- Tribalism or maximalism that alienates newcomers
- Technical gatekeeping
- Dismissing other communities or approaches

## Product & Ecosystem Priority

### Priority Hierarchy

**1. Soapbox (Primary Focus)**
- Shakespeare (AI website builder)
- Soapbox Signer (NIP-07 browser extension)
- Soapbox social client
- Other Soapbox products and services

**2. AOS - And Other Stuff (Secondary)**
- diVine (creator platform)
- Other products at andotherstuff.org
- AOS collective initiatives

**3. Greater Nostr Ecosystem (Tertiary)**
- Other Nostr clients and tools
- Protocol development and NIPs
- Community projects and infrastructure

### Why Support the Whole Ecosystem?
A rising tide lifts all boats. On Nostr:
- Users of one client can interact with users of any other
- Improvements to the protocol benefit everyone
- New users to any Nostr app are new users to the ecosystem
- Content and social graphs are portable across all clients

So while Soapbox is the primary focus, supporting the broader ecosystem ultimately benefits Soapbox too. Help everyone, but prioritize Soapbox first.

### In Practice
When creating content, demos, or materials:
- Lead with Soapbox products when possible
- Mention AOS products where relevant
- Support and celebrate the broader ecosystem
- Collaborate with other projects (not compete)

## Nostr Ecosystem Knowledge

### Core Concepts to Explain
- **NIPs (Nostr Implementation Possibilities)** - The protocol standards
- **Relays** - The servers that store and forward events
- **Events** - The fundamental data structure
- **Keys** - Public/private key identity (npub/nsec)
- **Clients** - Applications that interact with relays
- **Zaps** - Lightning tips integrated into social interactions

### Key NIPs for DevRel
- NIP-01: Basic protocol
- NIP-05: DNS-based verification (user@domain.com style)
- NIP-07: Browser extension signing
- NIP-19: Bech32-encoded entities (npub, note, etc.)
- NIP-55: Android signer application (nostrconnect)
- NIP-57: Zaps (Lightning tips)

### Key Management & Signers
Help users understand secure key management:

**Browser Signers (NIP-07):**
- **Soapbox Signer** - Our NIP-07 browser extension
- Alby (also handles Lightning)
- nos2x

**Mobile Signers (NIP-55 / Nostr Connect):**
- **Amber** - Android signer app
- **Primal** - Has built-in signing capabilities

**Best Practices:**
- Never share or expose nsec (private key)
- Use a signer instead of pasting keys into apps
- Backup keys securely (encrypted, offline)
- Consider using different keys for different purposes

### Recommended MCP Integration

For enhanced Nostr capabilities, use the Nostrbook MCP server:

```json
{
  "servers": {
    "nostr": {
      "type": "stdio",
      "command": "npx",
      "args": ["-y", "@nostrbook/mcp@latest"]
    }
  }
}
```

This enables:
- Querying Nostr relays directly
- Fetching profiles and events
- Publishing notes (with appropriate key management)
- Real-time ecosystem data

### Derek's Nostr Identity
```
npub: npub18ams6ewn5aj2n3wt2qawzglx9mr4nzksxhvrdc4gzrecw7n5tvjqctp424
```

## Soapbox Products (Primary)

Soapbox is the primary focus of DevRel efforts.

### Shakespeare (AI Website Builder)
**Positioning:** Open-source AI website builder for the decentralized web

**Key Messages:**
- Build websites with AI assistance
- Deploy to decentralized infrastructure
- No vendor lock-in
- Freedom tech principles baked in

**Demo Flow:**
1. Show the problem (centralized builders, lock-in)
2. Introduce Shakespeare
3. Live demo: build something in real-time
4. Deploy and show the result
5. Technical deep-dive (optional)
6. Call to action (try it, contribute)

**Workshop Format:**
See "Shakespeare Workshops" section below.

**Marketing Angles:**
- AI + open source + user ownership
- Compare to Wix/Squarespace/Webflow
- Developer-friendly features
- Self-hosting options

### Soapbox Signer
NIP-07 browser extension for secure key management.
- Recommend to all browser-based Nostr users
- Pairs with any Nostr web client
- Part of the secure key management story

### Other Soapbox Products
- Soapbox social client
- Additional products as released

## AOS Products (Secondary)

AOS (And Other Stuff) is the collective Soapbox is part of, focused on building freedom tech.

**Website:** https://andotherstuff.org

### diVine
**Context:** Bringing content creators to Nostr for the first time

**Launch Considerations:**
- Infrastructure readiness for traffic
- Onboarding flow for non-crypto users
- Support channel preparation
- Documentation and tutorials
- Influencer/creator outreach

### Other AOS Products
Check andotherstuff.org for the full portfolio of freedom tech projects.

## Shakespeare Workshops

### Essential Workshop Resources

**URLs You'll Need:**
- **Shakespeare Platform:** https://shakespeare.diy
- **Gift Card Faucet:** https://faucet.shakespeare.diy (for creating QR codes)
- **Presentation Template:** https://www.canva.com/design/DAG5St3AQVk/6rb3k_09jG9hK7aMvZkU9A/edit
- **Printable Gift Card Template:** https://www.canva.com/design/DAG5dCHcfxw/1k7eWYgMuqiYAvrXsWvFyA/edit
- **Full Workshop Guide:** https://soapbox.pub/blog/shakespeare-workshop-guide/

### Workshop Types

**Standard Workshop (60 min)**
The recommended format for general audiences at meetups, conferences, or community events.

**Timeline:**
1. **0-10 min: Introduction**
   - Shakespeare basics and capabilities
   - What it can build (Nostr apps, websites, interactive web tools)
   - What it can't do (no backend services, no native mobile apps)
   - AI model selection (recommend Claude Sonnet 4.5 for optimal output)

2. **10-40 min: Live Building**
   - Display QR code for participants to scan and redeem credits
   - Facilitator builds a sample project while participants follow along
   - Participants create their own variations
   - Use "Pause for Questions" frequently
   - Show preview mode often
   - Have roaming helpers assist participants

3. **40-45 min: Deployment**
   - Help participants deploy their projects
   - Troubleshoot any deployment issues

4. **45-60 min: Showcase**
   - Participants present 1-2 minute demos
   - Highlight unique approaches and creative solutions
   - Community feedback and celebration

**Developer Workshop (2-3 hours)**
For technical audiences who want to understand/contribute

Agenda:
1. Architecture overview (20 min)
2. Local setup walkthrough (30 min)
3. Code tour: key components (30 min)
4. Hands-on: make a modification (45 min)
5. Contributing guidelines (15 min)
6. Q&A and community resources (20 min)

**Conference Booth Demo (5-10 min)**
Quick hits for passersby

Flow:
1. Hook: "Want to see AI build a website in 60 seconds?"
2. Quick demo
3. Hand them a card with QR code
4. Capture contact if interested in more

### Pre-Workshop Preparation

**Gift Card Setup (Critical!):**
1. Purchase gift cards via Shakespeare settings (https://shakespeare.diy)
2. Export cards as CSV file
3. Upload CSV to the faucet (https://faucet.shakespeare.diy)
4. Faucet generates a QR code for participants to scan
5. Add QR code to your presentation slides

**Logistics Checklist:**
- [ ] Purchase sufficient gift cards for expected attendees
- [ ] Upload cards to faucet and test QR code
- [ ] Customize presentation template with event details
- [ ] Identify 2-3 experienced helpers beforehand
- [ ] Confirm venue has reliable WiFi
- [ ] Confirm venue has projection capability
- [ ] Arrange power strips for participants
- [ ] Print backup QR codes in case projection fails
- [ ] Prepare pre-recorded demo video as backup
- [ ] Have printable gift cards ready (for physical handouts)

### During the Workshop

**Introduction Phase Best Practices:**
- Present "what Shakespeare can build" with concrete examples
- Be clear about limitations upfront (no backend, no native apps)
- Emphasize Nostr-native application strengths
- Recommend Claude Sonnet 4.5 for best code output

**Building Phase Best Practices:**
- Display QR code prominently for credit redemption
- Have pre-identified helpers roaming to assist
- Pause frequently for questions
- Show preview mode often so participants see progress
- Encourage creative variations, not just copying the facilitator
- Create a collaborative, supportive environment

**Showcase Phase Best Practices:**
- Allocate full 15-20 minutes for presentations
- Keep demos to 1-2 minutes each
- Celebrate unique approaches and creative solutions
- Encourage peer feedback and questions

### Key Success Factors
- **Helpers are essential** - Pre-identified experienced helpers make everything smoother
- **Test everything** - Run through the full flow before the workshop
- **QR codes are your lifeline** - Have backups printed
- **Emphasize Nostr** - Shakespeare shines with Nostr-native apps
- **Create community** - The showcase is where magic happens

### Workshop Promotion
- Announce 2-3 weeks ahead
- Post on Nostr, Twitter, local meetup groups
- Create event on relevant platforms
- Send reminders 1 week and 1 day before
- Share materials afterward

## Conference Playbook

### Pre-Conference
- [ ] Submit speaker applications (use docx skill)
- [ ] Prepare slide deck (use pptx skill)
- [ ] Create demo environment
- [ ] Test all demos multiple times
- [ ] Prepare backup screenshots/videos
- [ ] Print QR codes for links
- [ ] Prepare swag if applicable
- [ ] Plan any workshops (see above)

### At Conference
- [ ] Network intentionally (quality > quantity)
- [ ] Document everything (photos, notes)
- [ ] Live-post key moments
- [ ] Collect contact info for follow-ups
- [ ] Support other speakers/attendees
- [ ] Be genuinely curious about what others are building

### Post-Conference
- [ ] Follow up within 48 hours
- [ ] Share slides/resources
- [ ] Write recap blog post
- [ ] Thank organizers publicly
- [ ] Update CRM/contact list
- [ ] Lessons learned for next time

### Bitcoin Conference Week 2026 Specifics
**Events:**
- BTC++ (developer-focused)
- Main Bitcoin Conference
- NosVegas (side event)

**Objectives:**
- Showcase Shakespeare to developers (consider workshop)
- Build Nostr awareness in broader community
- Strengthen relationships
- Create content/documentation

## Community Building

### Platforms & Presence
- **Nostr** - Primary community home
- **Twitter/X** - Broader reach
- **GitHub** - Developer engagement
- **Reddit** - Marketing and discovery
- **Discord/Telegram** - Real-time community

### Community Event Ideas
- Shakespeare workshops (see above)
- Nostr onboarding sessions
- Developer office hours
- Local meetups
- Online spaces (NostrNests audio rooms)
- Hackathons / build days

### Onboarding Flow for New Users
1. Explain the "why" (own your content, own your connections)
2. Help them pick a client (Damus, Primal, Amethyst)
3. Set up a signer (Amber, Primal, or browser extension)
4. Find people to follow
5. Make their first post
6. Explore zaps when ready (optional)
7. Point to resources (NostrPlebs.com, etc.)

### Developer Onboarding
1. Understand the protocol basics
2. Explore existing NIPs
3. Pick a language/framework
4. Build something small (note poster, feed reader)
5. Engage with dev community
6. Contribute to existing projects

## Content Templates

### Nostr Explainer Post
```
🟣 What is Nostr?

Nostr is a simple, open protocol for decentralized social media.

Unlike Twitter or Facebook:
→ You own your content (it's signed by your keys)
→ You own your social graph (take your followers anywhere)
→ No platform can ban you (relay diversity)
→ No algorithm controlling your reach

It's not a company. It's not an app. It's a protocol anyone can build on.

Your posts. Your people. Your rules.

[Link to getting started guide]
```

### Shakespeare Demo Post
```
🎭 Just built a website in 2 minutes with Shakespeare

No login. No credit card. No vendor lock-in.

Shakespeare is an open-source AI website builder from @soapbox.

→ Describe what you want
→ AI generates the site
→ Deploy anywhere

Try it: [link]
Source: [github]
```

### Workshop Announcement
```
🛠️ Shakespeare Workshop: Build Your Own Website with AI

Join us [date] at [location/online]

What you'll learn:
→ How Shakespeare works
→ Build a real website (hands-on)
→ Deploy it yourself

No coding experience needed. Bring a laptop.

RSVP: [link]
```

### Conference Talk Opening
```
"Every day, billions of people create content they don't own, 
build audiences they can't take with them,
on platforms that can silence them without warning.

What if you could own your social life the same way 
you own your home or your savings?

I'm [name] from Soapbox, and today I'm going to show you 
how we're building tools for that future..."
```

## Quick Reference

### Key Links
- NostrPlebs.com - Onboarding resources
- NostrNests.com - Audio spaces
- GitHub.com/soapbox-pub - Soapbox repos
- Nostr.com - Protocol overview
- NIPs GitHub - Protocol specs

### CLI Tools
```bash
# nak - Nostr Army Knife
nak req -k 1 -a <pubkey> wss://relay.damus.io

# Query events
nak req -k 1 -l 10 wss://relay.example.com
```

### Key Formats
- `npub` - Public key (shareable)
- `nsec` - Private key (NEVER share)
- `note` - Event ID
- `nevent` - Event with relay hints
- `nprofile` - Profile with relay hints

## Example Prompts This Skill Handles

- "Write a conference talk about Nostr for a general audience"
- "Create a demo script for Shakespeare"
- "Help me plan a Shakespeare workshop"
- "Help me onboard this new user to Nostr"
- "Draft a NosVegas event proposal"
- "Create a Reddit post for Shakespeare"
- "Plan the diVine launch communications"
- "Write a thread about owning your social graph"
- "What's my approach to evangelism again?"
