# TODO

The atomic task list for MAIS Log. Hierarchical: tasks → subtasks. Checked
when complete.

This is not a sprint backlog. It is a long-horizon map. Some sections are
years away. The order is roughly sequential within phases but tasks across
phases run concurrently.

**Versioning of this TODO**: append-only with revision notes at the bottom
when scope changes meaningfully. Day-to-day checking-off doesn't require
revision notes.

---

## Phase 0 — Repository scaffolding (MAJOR: v0.1.0)

**Goal**: a working repo that builds, deploys, and is ready to receive
writing. No content yet beyond the README and section indexes.

### 0.1 Repo initialization

- [x] Create directory structure (`content/`, `templates/`, `static/`,
      `sass/`, `docs/`, `_drafts/`)
- [x] Write README.md with the locked content
- [x] Write LICENSE.md (CC BY 4.0 prose, MIT OR Apache-2.0 code)
- [x] Write .gitignore
- [x] Write .editorconfig
- [x] Initialize Zola config.toml
- [x] `git init` and first commit (the README + licenses)
- [x] Create `github.com/SHA888/mais-log` repo (public)
- [x] Push initial commit
- [x] Verify repo is visible and licenses are detected by GitHub

### 0.2 Zola scaffold

- [x] Section index: `content/notes/_index.md`
- [x] Section index: `content/synthesis/_index.md`
- [x] Section index: `content/essays/_index.md`
- [x] About page: `content/about/_index.md`
- [x] Site landing: `content/_index.md`
- [x] Base template: `templates/base.html`
- [x] Index template: `templates/index.html`
- [x] Section template: `templates/section.html`
- [x] Page template: `templates/page.html`
- [x] Tag templates: `templates/tags/single.html`, `templates/tags/list.html`
- [x] Revision shortcode: `templates/shortcodes/revision.html`
- [x] Minimal stylesheet: `sass/main.scss`
- [x] robots.txt with AI crawler opt-out
- [x] Install Zola locally; verify `zola build` succeeds
- [x] Verify `zola serve` renders the site as expected
- [x] Iterate on stylesheet until reading the site is comfortable

### 0.3 Documentation

- [x] STYLE.md — voice, tone, conventions
- [x] WORKFLOW.md — drafting, publishing, editing flow
- [x] CONTRIBUTING.md — what's welcome, what's not
- [x] TODO.md — this file
- [x] Add favicon (low priority; can be a placeholder initially)

### 0.4 Domain and deploy

- [x] Acquire `sha888.id`
- [x] Decide deploy target: GitHub Pages, Cloudflare Pages, Netlify, or
      self-hosted VPS
  - [x] Evaluate: cost, build pipeline, custom domain support, longevity
  - [x] Take a position; document the choice in WORKFLOW.md
- [x] Configure CI: build Zola on push to `main`, deploy to chosen target
- [ ] Configure DNS: point `sha888.id` at the deploy target
- [ ] Verify HTTPS works end-to-end
- [ ] Verify Atom feed at `https://sha888.id/atom.xml`
- [ ] Verify Mastodon `rel="me"` verification works

### 0.5 Tagging release v0.1.0

- [ ] Site builds, deploys, is reachable at `https://sha888.id`
- [ ] All four documentation files are in place
- [ ] All three section index pages render
- [ ] Tag `v0.1.0` in git: "Repository scaffolded; first writing pending"

---

## Phase 1 — First content (MINOR: v0.2.0)

**Goal**: prove the workflow works. First note published. First reading
discipline started.

### 1.1 First note

- [ ] Draft the first note in `_drafts/`
  - Working title candidates: "What I plan to read first, and why" /
    "Starting from a low baseline" / "Why MAIS Log"
- [ ] Decide which working title fits best
- [ ] Move to `content/notes/2026-MM-DD-slug.md`
- [ ] Verify it builds and renders correctly
- [ ] Push and deploy
- [ ] Tag `v0.2.0` in git: "First note published"

### 1.2 Reading list as a living document

- [ ] Create `_drafts/reading-list.md` (or commit as `content/about/reading.md`
      if I want it visible)
  - Decide: visible reading list, or private to drafts?
- [ ] Populate with the M / A / C stream lists from the conversation
- [ ] Mark which I have read, which I am reading, which is queued
- [ ] Update as I move through it

### 1.3 Begin Stream M reading (Mechanics — largest gap)

- [ ] Read Saltzer & Schroeder, "The Protection of Information in Computer
      Systems" (1975)
  - [ ] First read
  - [ ] Write a note: what landed, what I missed
  - [ ] Schedule a re-read in 6 months
- [ ] Acquire Anderson, _Security Engineering_ (3rd ed., free online)
- [ ] Read Anderson, chapters 1–3
  - [ ] Chapter 1: What is security engineering?
  - [ ] Chapter 2: Who is the opponent?
  - [ ] Chapter 3: Psychology and usability
  - [ ] Write a note synthesizing the first three chapters
- [ ] Continue Anderson, one chapter every 1–2 weeks, for the year

### 1.4 Begin Stream A reading (Attack surface — secondary)

- [ ] Subscribe / bookmark the writeup sources:
  - [ ] Google Project Zero blog
  - [ ] Krebs on Security
  - [ ] Trail of Bits engineering blog
  - [ ] NCC Group research
  - [ ] Pwn2Own writeups (search-driven)
- [ ] Read 2–3 writeups per week
- [ ] After every 10 writeups, write a note synthesizing patterns observed

### 1.5 Begin Stream C reading (Consequence — tertiary)

- [ ] Acquire and read FDA pre-market cybersecurity guidance for medical
      devices (2023 update)
- [ ] Read EU MDR Annex I §17.2
- [ ] Read WHO _Ethics & Governance of AI for Health_ (2021)
- [ ] Read James Reason, _Human Error_ OR _Managing the Risks of
      Organizational Accidents_ (one, not both)
  - [ ] Decide which
  - [ ] Read
  - [ ] Write a note on how Reason's frame fuses with security incident
        analysis

---

## Phase 2 — Establish writing cadence (MINOR: v0.3.0)

**Goal**: the three publication tracks are all running. Cadence is
established as practice, not aspiration.

### 2.1 Notes track running

- [ ] Publish at least 4 notes (rough proxy for "monthly cadence
      established")
- [ ] Confirm the workflow (draft → publish → maybe edit) feels natural
- [ ] Adjust workflow document if practice diverges from documentation

### 2.2 First synthesis piece

- [ ] Draft the first monthly synthesis
  - Topic candidate: synthesizing patterns from the first month of notes
- [ ] Apply the AMC lens explicitly in the structure
- [ ] Move to `content/synthesis/YYYY-MM-slug.md`
- [ ] Verify rendering, publish

### 2.3 Bilingual question

- [ ] Decide: do I publish Indonesian-language versions of any pieces in
      year 1, or wait until year 2+?
- [ ] If yes: write the first Indonesian-language note
- [ ] If no: document the decision in WORKFLOW.md and revisit at v0.4.0

### 2.4 Tag v0.3.0

- [ ] At least 4 notes published
- [ ] At least 1 synthesis published
- [ ] Tag: "Writing cadence established"

---

## Phase 3 — First quarterly essay (MAJOR: v1.0.0)

**Goal**: the first substantial essay published. The site stops being a
scaffold-with-notes and becomes a published corpus.

### 3.1 The landscape review essay

This is the planned first quarterly piece: a landscape review of public
work at the intersection of clinical practice, AI/ML systems, and security.
Tests the hypothesis that the intersection is unoccupied.

- [ ] Define the search scope explicitly
  - [ ] Geographic: global, with attention to Indonesia and Southeast Asia
  - [ ] Disciplinary: clinical informatics, AI security, medical device
        security, healthcare cybersecurity
  - [ ] Time: last 5 years primarily, with classic foundational work where
        relevant
- [ ] Search systematically
  - [ ] Google Scholar searches for relevant terms
  - [ ] PubMed for clinical-side coverage
  - [ ] arXiv for AI-security-side coverage
  - [ ] Conference proceedings: USENIX Security, IEEE S&P, NDSS, AMIA, JAMIA
  - [ ] Industry research: Anthropic, OpenAI, Google DeepMind, Trail of
        Bits, NCC Group, Adversa AI, HiddenLayer, Robust Intelligence
  - [ ] Indonesian-context: BSSN publications, Kemenkes guidance, BPOM
        positioning
- [ ] Build a working bibliography
- [ ] For each candidate occupant of the intersection: write a one-paragraph
      note on what they cover and what they don't
- [ ] Synthesize: is the intersection occupied, partially occupied, or
      unoccupied? What does the answer change?
- [ ] Apply AMC structure: A (who is working where), M (how the work breaks
      down by mechanics), C (what each line of work treats as consequence)
- [ ] Write the essay (5000+ words)
- [ ] Have a candid second pass: is it honest about gaps? Does it terminate
      in C?
- [ ] Publish to `content/essays/2026-Q3-landscape-review/index.md`
- [ ] Tag `v1.0.0` — first essay is the milestone that makes this a real
      corpus

### 3.2 Reflect on the landscape

- [ ] Based on what the landscape review found, decide: do I continue with
      the working hypothesis, or does the roadmap need to update?
- [ ] If others are working in this space: identify which ones are likely
      collaborators; document for future outreach
- [ ] Write a note on what the landscape review changed in my thinking

---

## Phase 4 — Year 1 closure (MINOR: v1.1.0)

**Goal**: a full year of writing in the bag. The trajectory is visible.

### 4.1 Cadence sustained

- [ ] ~40+ notes published over the year (allowing for irregular weeks)
- [ ] ~10+ synthesis pieces (monthly target)
- [ ] 4 essays (quarterly target)
- [ ] Anderson read at least through chapter 12 (rough target)

### 4.2 First-year retrospective

- [ ] Write a retrospective synthesis or essay: "Year 1 of MAIS Log: what
      the trajectory looks like in retrospect"
- [ ] Honest assessment: which gaps closed, which didn't, which new gaps
      emerged
- [ ] Decide what changes for year 2

### 4.3 Tag v1.1.0

- [ ] Year 1 closure documented

---

## Phase 5 — Years 2–5 (MAJOR: v2.0.0 and beyond)

**Goal**: deepen each pillar. AMC stops being a fresh framework and
becomes reflexive.

### 5.1 Stream M deepening

- [ ] Complete Anderson, _Security Engineering_
- [ ] Move to threat modeling depth: Shostack, _Threat Modeling_
- [ ] Begin acquiring depth in selected sub-areas of mechanics:
  - [ ] Network security and protocol failure modes
  - [ ] Web/API security (PortSwigger Academy end-to-end)
  - [ ] Identity, OAuth2/OIDC, SMART on FHIR
  - [ ] Cryptography failure modes (not algorithm trivia)
  - [ ] Supply chain security: SBOM, signing, dependency confusion

### 5.2 Stream A deepening

- [ ] Continue writeup-reading discipline; aim for 100+ writeups by end of
      year 2
- [ ] Begin minimum-viable hands-on work: HTB or THM, in service of model
      installation, not certification
- [ ] Replicate one published exploit per quarter

### 5.3 Stream B (AI security) starting

- [ ] Read OWASP LLM Top 10; write a critical review essay
- [ ] Replicate Greshake et al. on indirect prompt injection
- [ ] Read Carlini's body of work; replicate one paper
- [ ] Read Goodfellow on adversarial examples; understand the radiology AI
      implications
- [ ] Track the field: Simon Willison's blog, Lilian Weng's blog,
      Anthropic / OpenAI / DeepMind safety publications
- [ ] Begin replicating one AI security paper per quarter

### 5.4 Stream C deepening

- [ ] Read FDA Predetermined Change Control Plan framework
- [ ] Read MDCG guidance documents on cybersecurity
- [ ] Build fluency with Indonesian regulatory frame: Permenkes on health
      information systems, BSSN healthcare guidance, BPOM positioning
- [ ] Connect with clinical incident analysis methodology (Reason's Swiss
      cheese model is the start, not the end)

### 5.5 Medical device security depth (third pillar)

- [ ] Replicate one published medical device CVE in lab
- [ ] Threat model a real medical device end-to-end (gateway, infusion
      pump, PACS node)
- [ ] Write a comparative regulatory analysis: FDA vs EU MDR vs BPOM on
      the same threat class

### 5.6 First Sec4MedicalAI synthesis

- [ ] Write a substantial essay (year 3-ish): full threat model of a
      clinical AI deployment, AMC throughout, technically defensible to
      Sec4AI researchers, clinically defensible to critical care physicians,
      regulatorily defensible to BSSN-class regulators

---

## Phase 6 — Years 5–10 (the long arc)

**Goal**: junction is — verified or unverified — occupied through public
artifacts. Sec4MedicalAI is recognizable as a discipline locally, and
MAIS Log is its working reference.

### 6.1 Public anchoring

- [ ] PERSI conference presentations
- [ ] BSSN engagement on medical AI security guidance
- [ ] Standards work: IEC 81001-5-1 regional implementation
- [ ] Academic publication: 1+ paper per year in venues like _Nature
      Digital Medicine_, _JAMIA_, _npj Digital Medicine_, USENIX Security,
      IEEE S&P (mix of clinical and security venues)

### 6.2 Community formation

- [ ] Mentorship: students in the Universitas Udayana fellowship
- [ ] Open-source: vigilimed, hl7-rs, id-siber-index continue as the
      technical artifacts
- [ ] Cross-disciplinary collaboration: identified from the year-1
      landscape review and refreshed periodically

### 6.3 Indonesian-language corpus

- [ ] By year 5, the Indonesian-language corpus on Sec4MedicalAI exists
      and is non-trivial
- [ ] Cross-link with English-language corpus where each version is
      deliberate, not auto-translated

---

## Standing tasks (continuous)

These don't fit a phase; they run throughout.

### Reading discipline

- [ ] Anderson chapter every 1–2 weeks, until complete
- [ ] 2–3 attack writeups per week
- [ ] AI security paper(s) when published; replicate one per quarter
- [ ] Regulatory texts: refresh annually as guidance evolves
- [ ] Reading list document kept current

### Writing discipline

- [ ] Weekly: at least one note (irregular but real)
- [ ] Monthly: at least one synthesis piece
- [ ] Quarterly: at least one essay
- [ ] Per-post: AMC lens applied consciously; post terminates in C if it's
      a substantial analysis

### OPSEC discipline

- [ ] Quarterly review: re-read everything published under SHA888 and ask
      what it discloses that I didn't intend
- [ ] Cross-site separation: kresnasucandra.com and sha888.id remain
      separable — they do not link to each other
- [ ] No specific patient references, even sanitized
- [ ] No specific institutional infrastructure references
- [ ] EXIF stripping on any images
- [ ] Mastodon timeline OPSEC: be mindful of what timing/location signals
      posts disclose

### Repository hygiene

- [ ] Quarterly backup push to a second remote (Codeberg or self-hosted
      Gitea)
- [ ] Annual review: STYLE.md, WORKFLOW.md, CONTRIBUTING.md still match
      practice
- [ ] Update TODO.md with revision notes when scope changes meaningfully

---

## Things that are not on this TODO (deliberate exclusions)

- **HTB rank, OSCP, CEH, or other certifications.** Not the goal. May
  pursue minimum-viable hands-on work in service of model installation,
  but not certification as an outcome.
- **Original vulnerability research output as a year-1 goal.** Premature.
  Year 3+ at earliest, if at all.
- **Tooling for security work (vigilimed, etc.).** Tracked separately;
  this TODO is for the writing corpus.
- **Speaking and conference output as year-1 goal.** Year 2+.
- **Cross-posting to Substack/Medium/LinkedIn.** Not part of the
  publishing strategy. The site is the canonical home.

---

## Revisions

_(None yet. When this TODO's scope changes meaningfully, append a revision
note here with the date and rationale. Day-to-day checking-off does not
require a revision note.)_
