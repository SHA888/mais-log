# Style guide

A living document. Future-me in 2034 will appreciate knowing the
conventions of past-me.

## Voice

- First person. "I" is fine. "We" is reserved for genuinely shared work
  with named collaborators.
- Direct over hedged. State positions; flag uncertainty explicitly when it
  matters; don't pad with weasel words.
- Honest about gaps. "I don't know yet" is a valid sentence.
- Evidence-grounded. Claims about the present-day world need verification,
  not memory.

## Tone

- Lower tone over higher tone. Avoid junction-occupation language; avoid
  capture-the-flag framing. The motivation, not the claim.
- Humility about gaps; confidence about reasoning. The two are
  complementary, not contradictory.
- No false modesty. Stating what I actually know is honest, not arrogant.

## Punctuation

- Em dash without spaces — like this — for parenthetical interjection.
- Spaced en dash for ranges in flowing text: "5–10 years."
- Oxford comma in lists.
- Code in `backticks` inline; fenced for blocks.

## Headings

- Sentence case, not title case: "What this site is", not "What This Site
  Is".
- H1 only once per post (the title). Body uses H2 and below.
- Headings describe the section, not advertise it.

## Code blocks

- Always fenced with language hint:
  ```rust
  let x = 1;
  ```
- Never indented-code-block syntax (4-space prefix). Inconsistent rendering.
- Comments in code samples are part of the code; keep them tight.

## Citations

- Inline links for casual references.
- Full citation block at the end of essays and synthesis pieces, when
  citing primary sources (papers, regulatory documents, books).
- Format for primary sources: `Author. (Year). Title. Venue. URL.`

## AMC vocabulary

- The framework is **AMC**, written in bold capitals on first use per post.
- Pairs are referenced as "the layer model", "the threat actor model",
  etc., lowercase, in flowing prose.
- The reasoning order **A → M → C** is consistent. Don't shuffle.

## Indonesian-language posts

When/if posts are written in Bahasa Indonesia:

- File suffix: `.id.md` for the Indonesian version, no suffix for English.
- Both versions live in the same section directory.
- Front matter `lang = "id"` in Indonesian posts.
- Don't auto-translate; if a post has both versions, each is a deliberate
  piece, not a mirror.

## Names and terms

- "MAIS Log" — site name, capitalized.
- "MAIS" — acronym, capitalized.
- "AMC" — framework, capitalized.
- "Sec4MedicalAI", "Sec4AI", "AI4Sec" — capitalized as written.
- Real product/standard names: as the standard writes them (HL7 v2, FHIR
  R4, DICOM, SATUSEHAT, OWASP LLM Top 10).

## What to avoid

- Marketing language. No "leverages", no "synergies", no "transformative".
- Performative humility. Either be honest about what I don't know or move
  on.
- Performative authority. Don't claim depth I haven't demonstrated.
- Listicles for the sake of listicles. Lists are for genuinely enumerable
  things, not for breaking up prose.

## When I update this guide

This document is editable freely (like notes). When a convention emerges
in practice that conflicts with what's here, update this document and note
the change in the next note. The guide reflects practice, not aspiration.
