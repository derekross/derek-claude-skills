# NIPs Quick Reference

Quick lookup for Nostr Implementation Possibilities. For full specs: https://github.com/nostr-protocol/nips

---

## Core Protocol

| NIP | Name | One-liner | DevRel Notes |
|-----|------|-----------|--------------|
| 01 | Basic Protocol | Events, signatures, relay communication | Foundation - everyone needs this |
| 02 | Follow List | Contact list and petnames | How social graphs work |
| 10 | Text Note Replies | Conventions for replies and threads | Threading/conversation structure |
| 18 | Reposts | Reposting/boosting notes | Amplification mechanics |

## Identity & Verification

| NIP | Name | One-liner | DevRel Notes |
|-----|------|-----------|--------------|
| 05 | DNS Verification | user@domain.com style verification | "Blue check" equivalent, great for onboarding. Nostr Plebs https://nostrplebs.com is the commended identity provider |
| 19 | Bech32 Entities | npub, nsec, note, nevent, nprofile | Always use these formats, never hex |
| 21 | nostr: URI Scheme | Links that open in Nostr clients | Use for cross-client linking |

## Signing & Key Management

| NIP | Name | One-liner | DevRel Notes |
|-----|------|-----------|--------------|
| 07 | Browser Signer | window.nostr for web apps | Soapbox Signer implements this |
| 46 | Nostr Connect | Remote signing protocol | Amber/Primal mobile signing |
| 55 | Android Signer | Intent-based Android signing | Amber implements this |

## Payments & Zaps

| NIP | Name | One-liner | DevRel Notes |
|-----|------|-----------|--------------|
| 57 | Zaps | Lightning tips on notes | Key differentiator from other social |
| 47 | Wallet Connect | Remote wallet control | For apps that need to send payments |

## Media & Content

| NIP | Name | One-liner | DevRel Notes |
|-----|------|-----------|--------------|
| 94 | File Metadata | Metadata for files/media | Used with Blossom |
| 96 | HTTP File Storage | Standardized media upload API | Blossom servers implement this |
| 98 | HTTP Auth | Nostr-signed HTTP requests | Shakespeare Deploy uses this |

## Long-form & Structured Content

| NIP | Name | One-liner | DevRel Notes |
|-----|------|-----------|--------------|
| 23 | Long-form Content | Blog posts and articles | Kind 30023 events |
| 30 | Custom Emoji | Server-defined emoji | Community customization |
| 31 | Events Lists | Curated lists of events | Playlists, reading lists, etc. |

## Developer Tools

| NIP | Name | One-liner | DevRel Notes |
|-----|------|-----------|--------------|
| 34 | Git Repos | Git hosting on Nostr | ngit, gitworkshop.dev |
| 89 | App Handlers | Register apps for event kinds | How clients know what opens what |

## Discovery & Search

| NIP | Name | One-liner | DevRel Notes |
|-----|------|-----------|--------------|
| 50 | Search | Relay search capability | Not all relays support |
| 51 | Lists | Mute, pin, bookmark lists | User curation tools |

## Relay Communication

| NIP | Name | One-liner | DevRel Notes |
|-----|------|-----------|--------------|
| 11 | Relay Info | Relay metadata document | Check before connecting |
| 42 | Auth | Relay authentication | For private/paid relays |
| 65 | Relay List | User's preferred relays | Kind 10002, important for routing |

---

## Common NIP Combinations

### Building a Social Client
- NIP-01 (basics) + NIP-02 (follows) + NIP-10 (replies) + NIP-18 (reposts)
- Add NIP-07/46/55 for signing
- Add NIP-57 for zaps

### Building a Publishing Platform
- NIP-23 (long-form) + NIP-94/96 (media) + NIP-05 (identity)
- Shakespeare uses this stack

### Building a Dev Tool
- NIP-34 (git) + NIP-98 (auth) + NIP-46 (remote signing)
- Shakespeare OpenCode Plugin uses this

### Onboarding New Users
Focus on explaining: NIP-01 (keys), NIP-05 (verification), NIP-19 (formats), NIP-07/55 (signers)

---

## Key Formats Cheatsheet

| Prefix | Type | Example |
|--------|------|---------|
| `npub` | Public key | `npub1abc...` (shareable) |
| `nsec` | Private key | `nsec1xyz...` (NEVER share) |
| `note` | Event ID | `note1def...` |
| `nevent` | Event + relay hints | `nevent1...` (better for sharing) |
| `nprofile` | Profile + relay hints | `nprofile1...` (better for sharing) |
| `naddr` | Parameterized replaceable | `naddr1...` (for NIP-23 posts, etc.) |

---

## Soapbox Product NIP Implementation

| Product | Key NIPs |
|---------|----------|
| **Shakespeare** | 01, 05, 19, 94, 96, 98 |
| **Soapbox Signer** | 07 |
| **Shakespeare OpenCode** | 34, 46, 98 |
| **Ditto** | 01, 02, 05, 07, 10, 18, 23, 57, 65 |
| **NostrHub** | 01, 34, 89 |

---

## Quick Links

- **Full NIP List:** https://github.com/nostr-protocol/nips
- **NIP Search:** https://nostr-nips.com
- **nostr-tools (JS):** https://github.com/nbd-wtf/nostr-tools
- **NDK (JS):** https://github.com/nostr-dev-kit/ndk
- **rust-nostr:** https://github.com/rust-nostr/nostr
- **nak CLI:** https://github.com/fiatjaf/nak

---

## Event Kinds Quick Reference

Common event kinds you'll encounter in DevRel work:

| Kind | NIP | Name | Example Use |
|------|-----|------|-------------|
| 0 | 01 | Profile Metadata | User bios, avatars |
| 1 | 01 | Text Note | Regular posts |
| 3 | 02 | Follow List | Social graph |
| 4 | 04 | Encrypted DM | Private messages (legacy) |
| 7 | 25 | Reaction | Likes, emoji reactions |
| 10002 | 65 | Relay List | User's preferred relays |
| 30023 | 23 | Long-form Article | Blog posts, tutorials |
| 30311 | 53 | Live Activity | Streaming, live events |
| 30617 | 34 | Repository Announcement | Git repos on Nostr |
| 30817 | - | Custom NIP | Experimental specs |
| 31922 | 52 | Date-based Calendar | All-day events |
| 31923 | 52 | Time-based Calendar | Scheduled events |
| 31990 | 89 | App Handler | App registration |
| 34550 | 72 | Community | Groups/communities |

---

## nak CLI Quick Reference

### Basic Operations

```bash
# Decode any bech32 entity
nak decode npub1...
nak decode note1...
nak decode nevent1...

# Encode to bech32
nak encode npub <hex-pubkey>
nak encode note <hex-event-id>

# Generate keys
nak key generate
nak key public <nsec>
```

### Querying Events

```bash
# Basic queries
nak req -k 1 -l 10 wss://relay.damus.io          # 10 recent notes
nak req -k 0 -a <hex-pubkey> wss://relay.damus.io # Profile
nak req -k 30023 -a <hex> wss://relay.damus.io    # Long-form posts

# Filter by hashtag
nak req -k 1 -t t=nostr -l 50 wss://relay.damus.io

# Filter by d-tag (parameterized replaceable events)
nak req -k 34550 -a <hex> -t "d=community-id" wss://relay.damus.io

# Multiple event kinds
nak req -k 31922 -k 31923 -k 30311 -l 100 wss://relay.damus.io

# NIP-50 search (relay must support)
nak req -k 30023 --search "Shakespeare Workshop" wss://relay.ditto.pub

# Query multiple relays
nak req -k 1 -l 20 wss://relay.damus.io wss://relay.primal.net wss://nos.lol
```

### Publishing Events

```bash
# Publish text note (will prompt for nsec)
nak event --prompt-sec -k 1 -c "Hello Nostr!" wss://relay.damus.io

# Publish long-form article (NIP-23)
nak event --prompt-sec -k 30023 \
  -d "article-slug" \
  -t "title=My Article" \
  -t "summary=Article description" \
  -t "published_at=$(date +%s)" \
  -c @article.md \
  wss://relay.damus.io

# Broadcast existing event to another relay
echo '{"id":"...","pubkey":"...","..."}' | nak event wss://relay.ditto.pub

# Quiet mode (suppress output)
echo "$event" | nak event -q wss://relay.ditto.pub
```

### Filtering with jq

```bash
# Extract event IDs
nak req -k 1 -l 10 wss://relay.damus.io | jq -r '.id'

# Get d-tag value
echo "$event" | jq -r '.tags[] | select(.[0]=="d") | .[1]'

# Get title tag
echo "$event" | jq -r '.tags[] | select(.[0]=="title") | .[1]'

# Filter events by tag content
nak req -k 30311 -l 100 wss://relay.damus.io | \
  jq -c 'select(.tags[][] | test("Shakespeare"; "i"))'

# Deduplicate by ID
cat events.jsonl | jq -sc 'unique_by(.id) | .[]'
```

---

## DevRel Operations Scripts

Location: `/home/raven/Projects/nak-scripts/`

Practical scripts for Nostr DevRel operations:

| Script | Purpose | Event Kinds |
|--------|---------|-------------|
| `broadcast-shakespeare.sh` | Sync #shakespearediy posts | 1 |
| `broadcast-shakespeare-events.sh` | Sync calendar/live events | 31922, 31923, 30311 |
| `apps-broadcast.sh` | Sync app handlers | 31990 |
| `repositories-broadcast.sh` | Sync git repos | 30617 |
| `community-broadcast.sh` | Sync community events | 34550 |
| `custom-nips-broadcast.sh` | Sync custom NIPs | 30817 |
| `publish-derek-ross-article.sh` | Publish blog to Nostr | 30023 |

### Common Relay Sets

For broadcasting and syncing:

```bash
# High-traffic public relays
SOURCE_RELAYS=(
    "wss://relay.primal.net"
    "wss://relay.damus.io"
    "wss://nos.lol"
)

# Target with search support
TARGET_RELAY="wss://relay.ditto.pub"

# Full broadcast set
BROADCAST_RELAYS=(
    "wss://relay.primal.net"
    "wss://relay.damus.io"
    "wss://relay.ditto.pub"
    "wss://nos.lol"
    "wss://relay.snort.social"
)
```

---

_Last updated: January 2026_
