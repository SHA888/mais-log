# MAIS Log

*A learning log on Medical AI Security, written from a clinical perspective.*

## Who writes here

I'm SHA888, the writer of MAIS Log (Medical AI Security Log) — a critical
care physician and software engineer working in Indonesia. I build software
primarily in Rust, across medical informatics, AI/ML systems, and
infrastructure. My clinical work and my engineering work are real and
continuous; the choice to write here under a handle is deliberate, not
concealment.

This site exists because I want to learn at an intersection that interests
me: the security of medical AI systems, approached from the perspective of
someone who works clinically, builds clinical AI, and is studying security.
Whether anyone else is working at this intersection in a public way is
something I do not know yet, and finding out is part of the work this site
documents.

I am starting from a low baseline in traditional cybersecurity. This site
documents that journey.

## What this site is

A working corpus, written in public, on the security of medical AI systems.
It is not a tutorial site. It is a learning log that may, over years, become
a reference at least for future-me.

The horizon is 5–10 years. Early work will be naive. I am committing to
leaving it visible as part of the trajectory, not deleting it to maintain a
clean image.

I write because I believe writing is how thinking becomes durable, and
because the act of writing forces me to clarify what I actually understand
versus what I have only encountered.

## The framework I use — AMC

I organize what I write through a three-part lens I call **AMC**. It is not
a contribution to the field; it is a personal cognitive handle that
compresses six standard threat-modeling components into three pairs:

- **A — Attack surface**: where the system can be hit, and by whom
  (the layer model + the threat actor model)
- **M — Mechanics**: how the system breaks, and how it holds
  (the failure model + the defense model)
- **C — Consequence**: what the harm is, and who judges it
  (the clinical workflow model + the regulatory model)

I reason A → M → C in that order. Starting from C invites motivated
reasoning — projecting clinical concern onto threats that may not be real,
and missing threats that don't map cleanly to clinical harm. Starting from A
forces honest enumeration; M describes what's actually possible; C
interprets what it means clinically and regulatorily.

I try to make every substantial analysis terminate in C. Technical interest
without clinical or regulatory grounding is, for the work I want to do, just
technical interest.

## Why this intersection

I work from three areas of practice:

1. **Clinical and clinical-informatics** — practicing critical care
   physician with active engineering work on medical interoperability
   standards (HL7 v2, FHIR R4, DICOM) and Indonesia's health information
   exchange platform.

2. **AI/ML systems** — building production AI systems; currently more
   practitioner than security researcher in this layer.

3. **Security** — the area I am actively learning, which this site
   documents.

I am writing here because I have not been able to find public work that
brings these three together in a way that fits the context I work in. That
absence may reflect a real gap, or it may reflect that I have not looked
hard enough. Either is fine — both lead to writing worth doing.

I am not trying to be first. I am trying to learn carefully, in public, over
a long time.

## Publication tracks

Writing here is organized into three tracks with different cadences and
different standards.

### `/notes` — weekly thinking-in-public

Short pieces, 300–600 words. Written as I learn. Low polish by design.
Edited freely with visible git history; what you read may not be what was
originally pushed. If I change my mind, the diff is the record.

These are explicitly *not* authority pieces. They are learning logs.

### `/synthesis` — monthly pattern abstraction

Longer pieces, 1500–3000 words. Each synthesizes patterns across several
weeks of notes. Append-only with revision notes — once published,
substantive changes are documented in a `## Revisions` section at the bottom
of the post, not silently rewritten.

### `/essays` — quarterly substantial work

Long pieces, 5000+ words. The core writing of this site. Append-only with
revision notes. By design these are tri-lens — A, M, and C all present —
even when the weight across the three is uneven.

## My starting point

To set reader expectations:

- Clinical and clinical-informatics: deep, with active research output.
- AI/ML systems: practitioner-level, building toward research depth.
- Traditional cybersecurity: starting from a low baseline. The first year of
  writing will reflect that.
- Sec4AI specifically: reading-level familiarity with the standard
  frameworks; no original research output yet.
- Medical device security: protocol-side stronger; device-as-attack-surface
  weaker.
- Regulatory: clinical and Indonesian-context familiarity; building fluency
  with FDA, EU MDR, and broader medical-device cybersecurity guidance.

## Editing and revision policy

Asymmetric across tracks:

- **Notes**: editable freely. The git history is the record. If you
  —for any reason— cite a note, cite the commit hash.
- **Synthesis and essays**: append-only with explicit revision notes.
  Substantive changes appear as `## Revisions` at the bottom of the post
  with date and rationale. The original text remains visible.

This asymmetry exists because notes are explicitly thinking-in-progress,
while synthesis and essays are positions I am willing to be held to.

## License

All written content on this site is licensed under
**Creative Commons Attribution 4.0 International (CC BY 4.0)**.

Code samples within posts, unless otherwise noted, are licensed under
**MIT OR Apache-2.0** to align with the Rust ecosystem default.

See [LICENSE.md](LICENSE.md) for the full terms.

## Contact

- Mastodon: [@sha888@mastodon.social](https://mastodon.social/@sha888)
- GitHub: [@SHA888](https://github.com/SHA888)

---

*MAIS Log — started 2026-05-04. Horizon: 2031–2036. Currently: learning.*
