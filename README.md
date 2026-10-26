# Luma Memory Drive
## Product PRD / SRD / Product & Go-to-Market Concept
**Status:** Concept / discovery  
**Working product family:** Luma Memory Drive → Luma Memory Hub  
**Owner:** Ismail Hossain / Luma  
**Date:** 2026-10-26

---

## 1. Executive Summary

**Luma Memory Drive** is a plug-and-play physical media archive designed to give people a **Google Photos-like memory timeline without requiring a cloud subscription**.

The product combines:
- Physical HDD/SSD storage
- Luma's timeline and media-library experience
- Automatic organization and indexing
- Phone/computer/SD-card media import
- Offline browsing
- Search, albums, favorites, tags and memories
- Local-first ownership of original files
- Optional backup/mirroring rather than pretending one disk is a backup

### Core proposition

> **Your memories, physically yours, beautifully organized.**

The key product insight is that existing solutions tend to optimize for only one side:

| Category | Storage | Timeline/library | Plug & play | Cloud-independent | Consumer-friendly |
|---|---:|---:|---:|---:|---:|
| Ordinary external HDD | ✓ | ✗ | ✓ | ✓ | ✓ |
| ThePhotoStick-type products | ✓ | Limited | ✓ | ✓ | ✓ |
| Google Photos | ✗ | ✓ | ✓ | ✗ | ✓ |
| Synology Photos/NAS | ✓ | ✓ | Partial | ✓ | Partial |
| Immich/PhotoPrism | ✓ | ✓ | ✗ | ✓ | Technical |
| **Luma Memory Drive** | **✓** | **✓** | **✓** | **✓** | **Target** |

The opportunity is not to build another NAS. It is to make **personal media archiving feel like an appliance instead of a storage-management project**.

---

# 2. Product Vision

Luma should evolve from:

**"A Windows media library that can use your existing drives"**

into:

**"A physical home for your memories that already understands them."**

The device should behave less like an HDD and more like a **personal memory appliance**.

A user should be able to:
1. Plug it in.
2. Open Luma.
3. Import years of scattered photos/videos.
4. Wait while Luma organizes/indexes them.
5. Browse everything chronologically.
6. Disconnect the device and reconnect it later without losing the library.
7. Add new photos from a phone, SD card or computer.
8. Find old memories without remembering filenames or folders.

---

# 3. Problem

Personal photos and videos are increasingly fragmented across:
- Phones
- Old phones
- External HDDs
- USB drives
- SD cards
- Computers
- WhatsApp exports
- Social-media downloads
- Cloud services

Traditional storage preserves files but not **context**.

Cloud photo services provide context but introduce:
- Recurring cost
- Cloud dependency
- Privacy concerns
- Storage migration problems
- Uncertainty about long-term ownership

Existing self-hosted solutions can solve much of this, but often require:
- NAS hardware
- Server setup
- Docker/Linux knowledge
- Networking
- Maintenance
- Database management

### Luma's opportunity

Create the missing middle:

**The simplicity of an external drive + the experience of a modern photo library.**

---

# 4. Target Users

### Primary
- Families with 5–20+ years of photos/videos
- People migrating from multiple old phones/computers
- Users who dislike recurring cloud storage subscriptions
- Non-technical users who want physical ownership
- People with large personal video archives

### Secondary
- Photographers
- Videographers
- Researchers/documentarians
- Families preserving historical archives
- Diaspora families preserving family memories
- Users who already own several external drives

### Initial market wedge

Do not target everyone.

Start with:

**People who already have messy, valuable personal media archives and want a simpler alternative to "buy more cloud storage."**

---

# 5. Product Family

## Phase 1 — Luma Memory Drive

A high-quality external HDD/SSD sold with Luma integrated into the experience.

Possible capacities:
- 2 TB
- 4 TB
- 8 TB

Primary connection:
- USB-C
- USB-A compatibility

The device remains a normal filesystem underneath.

## Phase 2 — Luma Memory Hub

A small network appliance containing:
- Storage
- Low-power CPU
- Wi-Fi/Ethernet
- Luma server
- Phone backup service
- Browser/TV access

The Hub becomes the household's local memory server.

## Phase 3 — Luma Memory System

Optional multi-drive architecture:
- Primary memory drive
- Automatic secondary backup
- Health monitoring
- Drive replacement/migration
- Remote/local access options

---

# 6. Product Design / Physical Shape

## Design direction

Avoid the visual language of:
- NAS boxes
- Gaming hardware
- Rugged industrial drives
- Router equipment

Target:

**Quiet, premium, archival, domestic.**

### Proposed form

A compact vertical or horizontal slab approximately the footprint of a small hardcover book.

Characteristics:
- Rounded rectangular body
- Matte neutral enclosure
- Minimal branding
- Single subtle status light
- USB-C at rear
- Optional Ethernet on Hub version
- No unnecessary screen
- No visible fan if thermally feasible

### Visual philosophy

The device should look appropriate:
- On a desk
- Beside a TV
- On a bookshelf
- In a family living room

It should communicate **archive**, not **computer accessory**.

---

# 7. Industrial Design Concept

### Front
- Small Luma mark
- One unobtrusive status indicator

### Rear
- USB-C
- Optional USB-A
- Power
- Ethernet on Hub model
- Optional HDMI on future TV-oriented model

### Physical interaction
Almost none.

The product's primary interface is software.

The physical device should disappear into the user's environment.

---

# 8. Core User Experience

## First setup

**Plug in → Open Luma → Name your Memory Drive → Import**

Luma detects the device and initializes the library.

The user chooses:

- Import existing media
- Start empty
- Import selected folders
- Import another drive
- Import phone/SD card

## Import experience

Luma scans files without changing originals.

It extracts:
- Capture date
- Modified date
- File type
- Resolution
- Duration
- EXIF metadata
- Location when available
- Camera/device information when available

Date priority:

1. Embedded capture date
2. Other reliable media metadata
3. File modified date
4. Unknown/manual correction

The system must never silently rewrite original timestamps.

---

# 9. Timeline Model

The defining experience is a chronological memory timeline.

Example:

```text
2026
 ├── October
 │    ├── 26
 │    ├── 25
 │    └── 21
 ├── September
 └── August

2025
 ├── December
 ├── November
 └── ...
```

But the interface should feel like a modern media application, not a filesystem.

Possible views:
- Timeline
- Years
- Months
- Days
- Albums
- Favorites
- Tags
- People
- Places
- Memories
- Recently added
- On this day

---

# 10. Core Features

## Must-have MVP

### Library
- Timeline browsing
- Photos
- Videos
- Year/month/day grouping
- Search
- Favorites
- Albums
- Tags
- Folder/source filtering
- Offline cached browsing

### Import
- Existing folder import
- Existing external drive import
- SD card import
- Phone import
- Incremental imports
- Duplicate detection

### Media
- Full-resolution original access
- Thumbnail cache
- Video playback
- Default-app opening
- Basic metadata

### Reliability
- Drive identity independent of drive letter
- Catalog persistence
- Reconnect detection
- Interrupted import recovery
- Scan cancellation/resume
- Catalog integrity checks

### Memory features
- On this day
- Year-in-review
- Recently added
- Random memory
- Memory resurfacing

---

# 11. Differentiating Features

## 11.1 Memory Import

The user can plug in:

- Old HDD
- USB stick
- SD card
- Phone
- Computer folder

Luma merges the media into one chronological experience.

This should be a major product differentiator.

## 11.2 "Your files stay yours"

Original media remains ordinary files.

Suggested structure:

```text
Luma Memory Drive/
├── Media/
│   ├── Photos/
│   ├── Videos/
│   └── Imported/
└── Luma/
    ├── catalog.db
    ├── thumbnails/
    ├── metadata/
    └── configuration/
```

The application database is an organizational layer, not a proprietary container.

If Luma disappears, the user's actual photos and videos remain accessible.

## 11.3 Memory continuity

The product should understand that:

> A drive is storage, but a memory library is a persistent identity.

Drive identity should use stable identifiers such as:
- Volume GUID/serial
- Relative paths
- File identity metadata

Drive letters should never define library identity.

---

# 12. Duplicate Detection

The system should detect:
- Exact duplicates
- Same file copied under different names
- Likely duplicate photos
- Resized copies
- Near-identical media where feasible

Important:

**Never delete automatically.**

Instead:
- Show duplicates
- Explain why they are considered duplicates
- Let the user decide

---

# 13. Backup Philosophy

A single Luma Memory Drive is **not a backup**.

This must be explicit in both product design and messaging.

The system should eventually support:

### Level 1
One Memory Drive

### Level 2
Memory Drive + secondary backup drive

### Level 3
Two-drive mirrored Memory System

### Level 4
Optional cloud/off-site backup

The product should make creating a second copy extremely simple.

Potential UX:

**"Protect your memories" → Connect another drive → Start backup**

---

# 14. Technical Architecture

## Memory Drive

```text
Physical Storage
      │
      ▼
Filesystem
      │
      ├── Original Media
      │
      └── Luma Data
             ├── Catalog
             ├── Metadata
             ├── Thumbnails
             └── Indexes
```

## Desktop Luma

- Native Windows application
- Local catalog
- Local thumbnail cache
- Background indexing
- Offline-first browsing
- External-drive identity
- Resumable scans

## Future Hub

```text
Phone ─────┐
Laptop ────┼── Wi-Fi/Ethernet ── Luma Hub
TV ────────┤                         │
Tablet ────┘                         ▼
                              Memory Storage
```

The Hub exposes:
- Local web/app interface
- Mobile upload
- Media browsing
- TV access
- Backup management

---

# 15. Storage Strategy

## HDD

Advantages:
- Low cost per TB
- Ideal for large archives
- 4–16 TB+ feasible

Disadvantages:
- Slower random access
- Mechanical failure risk
- Less portable

## SSD

Advantages:
- Fast browsing
- Silent
- Shock resistant
- Better premium experience

Disadvantages:
- Higher cost/TB
- Large archive pricing becomes difficult

### Product recommendation

Start with HDD for the mainstream archive product.

Offer SSD as a premium model.

Use local SSD/NVMe caching in the future Hub where economically justified.

---

# 16. Software Architecture Requirements

### Catalog
Must persist:
- Source identity
- Relative path
- Media type
- Size
- Modified timestamp
- Capture timestamp
- Metadata
- Thumbnail state
- Availability state
- Import source
- User organization data

### Cache
- Persistent thumbnails
- Bounded storage
- LRU eviction
- Atomic writes
- Versioned renderer/cache keys

### Indexing
- Background
- Resumable
- Cancellable
- Progress reporting
- No destructive operations
- Explicit refresh for discovery

### Offline mode
Known media should remain browsable when the physical drive is disconnected, subject to cached data.

---

# 17. Privacy Principles

Default architecture should be:

**Local first.**

No mandatory:
- Account
- Cloud subscription
- Telemetry
- Remote server
- AI API

Optional cloud/AI features may exist later.

If AI is added:
- Prefer on-device inference
- Make cloud processing explicit
- Explain what leaves the device

---

# 18. AI / Smart Organization Roadmap

AI should not be the initial reason to buy the product.

Useful later capabilities:

- Face grouping
- Object recognition
- Scene classification
- Places
- Automatic event grouping
- Similar-photo detection
- Natural-language search
- "Show me our trips to Cox's Bazar"
- "Find photos from university days"
- "Show photos with my family"

The timeline and ownership model must work without AI.

---

# 19. Product Safety / Trust Requirements

Because the product stores irreplaceable memories:

- No automatic destructive cleanup
- No silent file movement without user permission
- No hidden proprietary storage format
- Clear drive-health state
- Clear missing-media state
- Import recovery
- Database recovery
- Export capability
- Integrity verification
- Backup reminders
- Safe eject guidance

A **Memory Health** screen should eventually show:

```text
Memory Drive
Healthy

Storage: 4.1 TB / 8 TB
Media: 83,421 files
Videos: 6,102
Photos: 77,319

Catalog: Healthy
Index: Complete
Last backup: 3 days ago
Drive health: Good
```

---

# 20. Competitive Positioning

## ThePhotoStick

Strong:
- Simple physical backup
- Consumer-oriented

Weak:
- Primarily backup/import
- Not a deep persistent media-library experience

## Synology Photos

Strong:
- Excellent physical-storage + library combination
- Mature ecosystem

Weak:
- NAS purchase/setup
- More technical
- Broader than the specific memory-appliance problem

## Immich

Strong:
- Excellent Google Photos-like self-hosted experience
- Powerful timeline/search/AI

Weak:
- Server-first
- Technical setup
- Not a consumer appliance

## PhotoPrism

Strong:
- Excellent archive indexing
- Existing-folder philosophy

Weak:
- Self-hosted software
- Not a turnkey physical product

## Google Photos

Strong:
- Excellent consumer UX
- Search
- Timeline
- Automatic backup

Weak:
- Cloud dependency
- Subscription pressure at scale
- Physical ownership is secondary

### Luma's position

**Physical ownership + modern memory UX + appliance simplicity.**

---

# 21. Go-to-Market Strategy

## Phase 0 — Validate before hardware

Do not manufacture hardware first.

Use existing:
- Luma software
- External HDDs/SSDs
- Branded packaging
- Setup workflow

Create a **Luma Memory Drive prototype** using commercially available storage.

Test with 10–30 users.

Measure:
- Setup completion
- Import success
- Number of devices/media sources imported
- Timeline usefulness
- Duplicate usefulness
- Offline browsing
- Willingness to pay
- Backup adoption
- Retention after 30/90 days

## Phase 1 — Software + certified hardware

Sell:
- Luma software
- Recommended/validated HDD/SSD
- Optional enclosure
- Installation/setup

This minimizes hardware risk.

## Phase 2 — Branded product

Once demand is demonstrated:
- Custom enclosure
- Preconfigured drive
- Retail packaging
- Simple setup
- Warranty
- Support

## Phase 3 — Luma Memory Hub

Build the network appliance only after proving the library experience.

---

# 22. Business Model

Possible models:

### Hardware margin
Primary revenue.

### Software
Core Luma experience included.

Avoid making basic timeline functionality subscription-only.

### Optional paid services
- Cloud backup
- Off-site backup
- AI processing
- Extended warranty
- Drive replacement
- Multi-device backup

The central library should remain useful without recurring payment.

---

# 23. Indicative Product Tiers

Pricing must be validated against actual BOM, storage pricing, enclosure cost, support and distribution.

### Luma Memory Drive 2 TB
Entry model

### Luma Memory Drive 4 TB
Likely mainstream model

### Luma Memory Drive 8 TB
Large archive model

### Luma Memory SSD
Premium portable version

### Luma Memory Hub
Networked household model

Do not finalize retail prices until hardware BOM and target geography are researched.

---

# 24. Brand / Naming

### Preferred

**Luma Memory Drive**

Why:
- Direct
- Understandable
- Extensible
- Connected to existing Luma brand

### Future family

- Luma Memory Drive
- Luma Memory SSD
- Luma Memory Hub
- Luma Memory Backup
- Luma Memory System

Avoid names that sound like:
- Generic HDD brands
- NAS products
- Cloud services
- AI startups

---

# 25. Product Language

The product should consistently communicate:

**Ownership**
- Your files
- Your drive
- Your memories

**Simplicity**
- Plug in
- Import
- Browse

**Continuity**
- Years of memories in one place

**Trust**
- Originals remain yours
- No mandatory cloud
- No proprietary media container

Potential positioning statement:

> **Luma Memory Drive turns years of scattered photos and videos into one physical, chronological memory library.**

---

# 26. MVP Scope

### Include

- External drive detection
- Library initialization
- Import folders
- Import external drives
- Timeline
- Search
- Albums
- Favorites
- Tags
- Thumbnails
- Video playback
- Duplicate detection
- Offline catalog
- Reconnect handling
- Basic health
- Export/open original
- Backup-to-second-drive workflow

### Exclude initially

- Face recognition
- Generative AI
- Cloud sync
- Remote internet access
- Complex NAS features
- Multi-user permissions
- Surveillance/security-camera features
- Full media-server ecosystem

The first product must solve one problem exceptionally well:

**Organize and preserve personal memories.**

---

# 27. Validation Hypotheses

The product should only move toward custom hardware if these hypotheses prove true:

### H1
People value a physical, cloud-independent memory library.

### H2
People are willing to pay more for organization than for raw storage.

### H3
The timeline meaningfully changes how users interact with old archives.

### H4
Users prefer a dedicated appliance over configuring a NAS.

### H5
Automatic import and organization reduce enough friction to justify the product.

### H6
Users understand that one physical drive is storage, not backup.

### H7
Luma's existing software architecture can support the appliance without a complete rewrite.

---

# 28. Key Risks

| Risk | Severity | Mitigation |
|---|---|---|
| HDD failure | Critical | Backup workflow + health monitoring |
| Users expect backup but only buy one drive | Critical | Explicit backup model |
| Hardware support burden | High | Validate with off-the-shelf hardware first |
| Google Photos is "good enough" | High | Ownership + no subscription + physical archive |
| NAS products are cheaper/more capable | Medium | Simplicity, not feature competition |
| Import takes too long | High | Resumable indexing + useful progress |
| Metadata is inaccurate | High | Clear date hierarchy + manual correction |
| Custom hardware MOQ/cost | High | Delay custom hardware |
| AI increases complexity | Medium | Keep AI optional |
| Proprietary lock-in concerns | High | Normal filesystem originals |

---

# 29. Method / Product Development Approach

## Step 1 — Productize existing Luma

Use the current Luma architecture as the software foundation.

Do not fork the product unnecessarily.

## Step 2 — Build a simulated Memory Drive

Use:
- Existing HDD/SSD
- Fixed directory convention
- Luma onboarding
- Product-style setup flow

## Step 3 — Real-world archive testing

Test with:
- 100 GB
- 500 GB
- 1 TB
- 2 TB+
- Mixed photos/videos
- Multiple years
- Duplicate-heavy archives
- Broken/missing files
- Disconnected/reconnected drives

## Step 4 — User research

Give people their own messy archive and observe:

> "Show me what you remember from 2018."

Measure whether Luma actually helps them rediscover memories.

## Step 5 — Prototype packaging

Create a physical mockup and test:
- Size
- Shape
- Cable placement
- Desk/TV placement
- Perceived quality
- Setup clarity

## Step 6 — Pilot sales

Sell a small number of real units using existing drives.

Do not manufacture at scale yet.

## Step 7 — Hardware decision

Only after demand is demonstrated:

**Buy existing hardware → customize enclosure → custom electronics only if necessary.**

---

# 30. Long-Term Vision

The ultimate Luma product is not an HDD.

It is a **personal memory infrastructure**.

The physical drive is simply the trust anchor.

The experience becomes:

```text
                 LUMA
                  │
        ┌─────────┼─────────┐
        │         │         │
      Phone     Laptop      TV
        │         │         │
        └────── Memory Hub ─┘
                   │
             Memory Library
                   │
          ┌────────┴────────┐
       Primary            Backup
       Storage             Storage
```

The user's memories remain:
- Physically owned
- Chronologically organized
- Searchable
- Accessible across devices
- Portable
- Recoverable
- Independent of a single cloud provider

---

# 31. Product Verdict

**Commercial viability: promising, but hardware should not be the first bet.**

The strongest opportunity is not another external HDD.

It is:

> **A plug-and-play physical alternative to cloud photo libraries.**

Luma already has unusually relevant foundations for this concept:
- Timeline browsing
- External-drive identity
- Offline catalog
- Cached previews
- Reconnect handling
- Resumable indexing
- Memories
- Local-first architecture

The recommended path is therefore:

**Luma software → simulated Memory Drive → user pilot → validated hardware bundle → Luma Memory Drive → Luma Memory Hub.**

The most important strategic rule:

> **Do not build a NAS. Build the easiest way for an ordinary person to own and enjoy a lifetime of memories.**
