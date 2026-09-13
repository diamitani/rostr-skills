# rostr-skills

**Rostr skills: drop-in bot services for the Artispreneur label services marketplace.**

34 production skill packages (SKILL.md + references.md + manifest.json), each one a
priced, sellable bot service. Together they cover the independent artist's label
operations end to end — EPKs, bios, brand, contracts, PRO registration, releases,
royalties, taxes, merch, marketing, and more.

## Honest note: skills don't run by themselves

A skill is a work order, not a worker. Each folder contains instructions a bot
follows — but it needs a harness to execute:

- **Option A — Claude Code:** copy one skill folder into `~/.claude/skills/<name>/`
  and the skill becomes available to the agent immediately.
- **Option B — Claude Code plugin:** install this whole repo as a plugin via
  `/plugin` and all 33 skills load at once (see `plugin.json`).
- **Option C — the Rostr runtime:** point `rostr-core`'s
  `pal.compile(skill_path=...)` at any skill folder and a worker will execute
  it (see the rostr-core repo in this Drive folder's parent).

## Install

```bash
git clone <repo-url> rostr-skills
# Option A: one skill
cp -r rostr-skills/skills/create-an-epk ~/.claude/skills/create-an-epk
# Option B: whole plugin
# in Claude Code: /plugin add ./rostr-skills
```

## The catalog — 34 skills, $777 combined list price

### STUDIO → artistepks.com (4)

| Skill | Price | What the bot does |
|---|---|---|
| `create-an-artist-bio` | $12 | 50/150/400 word bios |
| `create-an-epk` | $29 | Full media kit / EPK |
| `create-brand-logo` | $19 | Wordmark/lockup brief |
| `write-brand-guidelines` | $29 | Voice/palette/type/merch rules enforced across marketing |

### DIRECTORY (1)

| Skill | Price | What the bot does |
|---|---|---|
| `find-outreach-targets` | $25 | Type a goal ("get on playlists", "book gigs") — finds best-matched playlists, venues, curators, promoters and writes tailored outreach messages |

### CONTRACTS (2)

| Skill | Price | What the bot does |
|---|---|---|
| `create-split-sheet-agreement` | $19 | Writer/producer splits before submission or distribution |
| `license-music` | $19 | Sync/license brief, licensing sub-capability |

### LABEL OPS (27)

| Skill | Price | What the bot does |
|---|---|---|
| `add-music-to-collaborative-playlist` | $15 | Playlist pitch, Indie Bible tone, part of Messaging/Sequences |
| `analyze-social-media-engagement` | $19 | Hook rate, saves, posting windows feeding paid media decisions |
| `build-a-skill` | $19 | Package a SKILL.md for preload |
| `build-an-agent` | $29 | Compile a Claude Code subagent markdown file |
| `claim-tracks-with-pro` | $15 | Claim unmatched performances/digital uses |
| `create-c-corp` | $79 | C-Corp outline for scale or investors |
| `create-content-calendar` | $15 | 30-day calendar for Scheduling and Posting |
| `create-llc` | $49 | State LLC formation brief and operating agreement draft |
| `create-lyric-video` | $19 | Timed lyric storyboard |
| `create-merch-designs` | $25 | SKU concepts for E-Commerce/Merch |
| `extract-metadata-from-track` | $9 | ISRC/writers/BPM/key JSON |
| `file-business-taxes` | $49 | Quarterly estimate + tax folder |
| `generate-social-media-content` | $15 | Hooks/captions for Content Creation |
| `get-ein` | $19 | Guided IRS EIN packet after entity choice |
| `manage-business-expenses` | $15 | Studio/ads/travel ledger |
| `open-business-bank-account` | $12 | Docs list + bank comparison |
| `register-tracks-with-pro` | $19 | Batch work registration + key sheet entry |
| `register-with-pro` | $15 | Artist/company PRO signup |
| `release-music-with-dsp` | $29 | Release ticket, 21-day buffer |
| `set-up-dsp` | $15 | Spotify/Apple/YouTube artist profile claim |
| `set-up-merch-drop-shipping` | $25 | POD vs warehouse for E-Commerce/Merch |
| `track-royalties-on-dsps` | $25 | Key-sheet-linked royalty pulse and gap alerts |
| `transcribe-lyrics` | $9 | Clean lyrics with section tags |
| `upload-music-video-to-youtube` | $12 | YouTube packet: title/desc/chapters, confirmed via API |
| `upload-track-to-catalogue` | $9 | Vault master with provenance |
| `write-a-business-plan` | $39 | 12-month plan with revenue mix |
| `write-music-video-treatment` | $25 | Scene-by-scene treatment with budget bands |


## Companion (not bundled)

**`artispreneur-music-contract-agent`** — the full contract agent skill
(drafts/reviews across 30 contract templates + 30 questionnaires) already lives
as its own GitHub repo (`diamitani/artispreneur-music-contract-skill`). The two
`contracts` skills above are its $19 entry slices.

## Source

Packaged from the Artispreneur v3 skill drop. SKILL.md and references.md are
verbatim; manifest.json was generated (price from the v3 list price, vertical
assignment, tool requirements from each skill's `allowed-tools`).
