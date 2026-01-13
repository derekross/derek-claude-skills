# AI Skills for Nostr DevRel

A collection of AI Skills for Developer Relations work in the Nostr ecosystem, focused on community building, content creation, and freedom tech advocacy.

Built for my work as DevRel at [Soapbox](https://github.com/soapbox-pub) and the [AOS (And Other Stuff)](https://andotherstuff.org) collective.

## What Are Skills?

Skills are folders containing instructions that teach AI assistants how to perform specific tasks. When you install a skill, your AI assistant automatically loads it when relevant to your request.

## Included Skills

| Skill | Description |
|-------|-------------|
| **nostr-devrel** | Nostr/freedom tech DevRel toolkit with philosophy, product priorities, workshop planning, conference prep, and community building workflows |
| **executive-assistant** | Task management, meeting notes, email drafting, document organization, and administrative workflows for subcontractors/consultants |
| **strategic-planning** | Create and execute strategic plans for conferences, product launches, and campaigns |
| **content-research-writer** | Research topics and create blog posts, Reddit campaigns, technical articles, and social content |
| **pptx** | Create professional PowerPoint presentations for conferences and demos |
| **docx** | Create Word documents including proposals, invoices, contracts, and documentation |
| **xlsx** | Create Excel spreadsheets for budgets, expense tracking, and project management |

## Installation

### OpenCode

```bash
# Clone the repo
git clone https://github.com/derekross/derek-claude-skills.git

# Create OpenCode's skills directory if it doesn't exist
mkdir -p ~/.opencode/skills

# Copy the skills you want
cp -r derek-claude-skills/nostr-devrel ~/.opencode/skills/
cp -r derek-claude-skills/executive-assistant ~/.opencode/skills/
cp -r derek-claude-skills/strategic-planning ~/.opencode/skills/
cp -r derek-claude-skills/content-research-writer ~/.opencode/skills/
cp -r derek-claude-skills/pptx ~/.opencode/skills/
cp -r derek-claude-skills/docx ~/.opencode/skills/
cp -r derek-claude-skills/xlsx ~/.opencode/skills/
```

## The Nostr DevRel Skill

This is the core skill, built around my approach to developer relations in the Nostr ecosystem.

### Core Philosophy

**Own Your Social Life** — Nostr empowers people to own their content, their social graph, their identity, and their reach.

**Relationship-First Approach** — Build relationships → Build trust → Adoption follows through osmosis. No preaching, no heavy-handed Bitcoin maximalism.

**Rising Tide Lifts All Boats** — Supporting the broader Nostr ecosystem benefits everyone, including Soapbox.

### Product Priority

1. **Soapbox** (Primary) — Shakespeare, Soapbox Signer, Soapbox client
2. **AOS** (Secondary) — diVine, andotherstuff.org products  
3. **Nostr Ecosystem** (Tertiary) — Other clients, NIPs, community projects

### Features

- Shakespeare workshop planning (intro, developer, booth demo formats)
- Conference playbook (pre/during/post checklists)
- Community building workflows
- Content templates for posts, threads, announcements
- Key management guidance (Soapbox Signer, Amber, Primal)
- MCP integration with Nostrbook

### Recommended MCP Integration

For live Nostr data, pair with the Nostrbook MCP server:

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

## Usage Examples

Once installed, your AI assistant will automatically invoke relevant skills. You can also be explicit:

```
"Help me plan a Shakespeare workshop for the Bitcoin conference"

"Create a presentation about Nostr for a non-technical audience"

"Draft a follow-up email to the conference organizer"

"What should my priorities be today?"

"Process these meeting notes into action items"

"Create a budget spreadsheet for the NosVegas event"
```

## Customization

These skills are tailored to my workflow, but you can fork and modify them for your own use:

- Update product names and priorities
- Add your own templates
- Adjust the philosophy to match your approach
- Add organization-specific guidelines

## Structure

```
├── nostr-devrel/
│   └── SKILL.md
├── executive-assistant/
│   └── SKILL.md
├── strategic-planning/
│   └── SKILL.md
├── content-research-writer/
│   └── SKILL.md
├── pptx/
│   └── SKILL.md
├── docx/
│   └── SKILL.md
├── xlsx/
│   └── SKILL.md
├── LICENSE
└── README.md
```

## Related Resources

- [Soapbox GitHub](https://github.com/soapbox-pub)
- [And Other Stuff](https://andotherstuff.org)
- [NostrPlebs](https://nostrplebs.com) — Nostr onboarding resources
- [NostrNests](https://nostrnests.com) — Audio spaces on Nostr

## License

MIT — See [LICENSE](LICENSE)

---

*"The purple pill helps the orange pill go down"* 🟣🟠

npub: `npub18ams6ewn5aj2n3wt2qawzglx9mr4nzksxhvrdc4gzrecw7n5tvjqctp424`
