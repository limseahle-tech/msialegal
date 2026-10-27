---
name: msia-submissions
description: "Use when Caroline asks to draft, restructure or review a Malaysian court Written Submission (main submission, in support of or in opposing an Enclosure) or a Submission in Reply. Runs a staged workflow (case intake, case map, issue matrix, outline, draft, self-review) and writes in Caroline's house style: Lum Kok Kiong & Co layout, CRUX-led structure, E-number pinpoints, bold-italic-underlined authorities, Arial 12 / 1.5 / auto-numbered Word output."
---

# Malaysian Written Submissions and Submissions in Reply

This skill drafts and reviews interlocutory and trial submissions for the Malaysian High Court in Caroline's own style. It covers four modes:

| Mode | Use when | Structure file |
|---|---|---|
| **Main – applicant** | "in support of Enclosure X" | `references/structure-main.md` (Variant A) |
| **Main – respondent** | "in opposing Enclosure X" | `references/structure-main.md` (Variant B) |
| **Reply – applicant** | reply "in further support of Enclosure X" | `references/structure-reply.md` |
| **Reply – respondent** | reply "in further opposing Enclosure X" | `references/structure-reply.md` |

Always also read `references/style-and-phrasing.md` before writing a sentence, and `references/review-checklist.md` before delivering.

## Hard rules (Caroline's standing instructions — these override any sample)

1. **Confidentiality.** Never upload, paste or send cause papers, drafts or client facts to any third-party service (including other AI drafting tools such as JusType). Research authorities only through Caroline's own signed-in research tools (see `lexis-my-research` skill) using generic legal queries, never client facts.
2. **Never delete** any file in a shared folder. Save new drafts as new files.
3. **Revising an existing draft:** type the amendments in chat (old text → new text, by paragraph number) with an apply option. Do not edit her document unless she asks for the file to be changed. Read tracked changes (`w:ins` / `w:del`) and comments first and treat accepted/pending changes as part of the current text.
4. **Authorities:** the whole case name **and** citation in ***bold + italic + underline***, e.g. ***<u>Press Metal Sarawak Sdn Bhd v Etiqa Takaful Bhd [2016] 5 MLJ 417 (FC)</u>***. Same for statutes/rules: ***<u>Order 4 Rule 1(1) of the ROC 2012</u>***.
5. **Pinpoints:** short square-bracket form — `[refer to paragraphs 13 to 26 of the Plaintiff's Submissions at E59/5-7]`.
6. **Brief and concise.** Every paragraph must advance the CRUX. **Never argue the same point twice** — make it once in full, then cross-refer ("as submitted at paragraph 14 above").
7. **Word format:** Arial 12, line spacing 1.5, automatic numbering, 0 pt before/after, an empty paragraph (Enter) between paragraphs, indentation Left 0.0" / Right 0.0" / Special: Hanging 0.5" for **all** paragraphs including sub-paragraphs. Use `scripts/build_submission.py` (see below), which enforces this. Where her older samples differ (they use a 0.49" left indent), the stated rule wins.
8. Apply the `avoid-ai-markers` skill to the finished text.

## Workflow

Work through the stages in order. Stop at the end of Stage 3 and show Caroline the outline before drafting in full unless she says to go straight to the draft.

### Stage 1 – Intake (build the record)

Read every primary document in full (never summaries): the Notice of Application, all affidavits, pleadings, and for a reply, both sides' Written Submissions and Bundles of Authorities.

- Large PDFs: `pdftotext -layout -f N -l N file.pdf -` page by page so you can map paragraph → PDF page for E-cites.
- .docx: `pandoc --track-changes=all file.docx -t markdown`.
- Record each document's **Enclosure number**, date, deponent and the short-form defined term. If an Enclosure number cannot be confirmed, use `[Enclosure ●]` and list it in the delivery note. Never guess.
- Record each authority's **Tab number and E-page** in the relevant BOA.

### Stage 2 – Case map

Produce (internally, or in chat if Caroline asks) a case map:

1. **Parties and defined terms** — D1…D5 / P1, P2, the defined terms used in the SOC or affidavits (keep them verbatim; never substitute an equivalent label).
2. **The application** — rules invoked, each prayer, defined name ("the said Application", "Stay Order", "Transfer & Consolidation Order").
3. **The governing test** — each limb, the provision and the leading authority (FC > CA > HC).
4. **Salient facts** — each with its E-cite; flag admissions and "not disputed" facts by the other side (these become CRUX ammunition).
5. **The other side's grounds** — each ground with its paragraph and E-cite in their affidavit or submissions.
6. **New points in their submissions not found in their affidavits** — candidates for a Preliminary Objection (statement from the bar).

### Stage 3 – Issue matrix and outline

For each limb of the test build one row: *limb → our position (one sentence) → evidence (E-cites) → authority (Tab/E) → their point → our answer*. Then:

- Collapse duplicate rows. If two of their grounds are answered by the same point, group them under one numbered paragraph with lettered sub-points.
- Write the **CRUX** (main: one introductory summary of their basis + lettered grounds; reply: their central contention + why it fails, 2-3 paragraphs maximum).
- Order sub-headings to follow the limbs of the test (main) or the other side's own headings (reply), each phrased as a proposition: "NO COMMON QUESTION OF LAW OR FACT", "THE PRESENCE OF NON-SIGNATORY DEFENDANTS DOES NOT DEFEAT A STAY".
- Present the outline to Caroline: headings, one line per numbered paragraph, authorities per section, and open questions.

### Stage 4 – Draft

Follow the structure file for the mode and `references/style-and-phrasing.md`. Draft section by section. For every factual assertion attach an E-cite; for every legal proposition attach an authority with Tab/E-cite or flag `[authority needed]`.

Quoting authorities: quote only the operative paragraph(s), in italics, with paragraph number in square brackets, key words in **bold** (and the decisive phrase **<u>bold underlined</u>**), followed by "(emphasis added)".

### Stage 5 – Self-review

Run every item in `references/review-checklist.md`. Fix what you can; list what needs Caroline (placeholders, unverified cites, strategic calls).

### Stage 6 – Deliver

- New draft: build the .docx with the script, render to PDF (`soffice --headless --convert-to pdf`) and check numbering and pagination visually, then send the file.
- Revision of her draft: amendments in chat, grouped by paragraph, each as `Para X: "old" → "new"` with a one-line reason, plus an apply option.
- Close with a short note: placeholders, unverified authorities, and any argument you think is weak — say so plainly.

## Building the Word document

`scripts/build_submission.py` turns a light markdown file into a formatted .docx (court header, parties table, title box, solicitors block, auto-numbered body, signature block and filed-by footer).

```
python3 scripts/build_submission.py draft.md -o "Pf Reply Submissions - E16 - v1.docx"
```

Input format is documented at the top of the script and in `assets/example-input.md`. Inline markup: `**bold**`, `*italic*`, `__underline__`, `[[Case Name [2016] 5 MLJ 417 (FC)]]` → bold + italic + underline, `^st^` → superscript.

## Related skills

- `lexis-my-research` — find and verify authorities (generic legal queries only).
- `malaysian-legislation-library` — statute text; always state the version date.
- `legal-pleading-fact-check` — check figures and facts against exhibits.
- `avoid-ai-markers` — final pass on wording.
- `malaysian-submissions-in-reply` — earlier, reply-only version of these rules; this skill supersedes it where they differ.
