# Review Checklist (run before delivering any draft or review)

Report findings in four groups with paragraph numbers: (A) grammar and terminology, (B) numbering and structure, (C) citations and record, (D) argument strength. Take tracked changes and comments into account first.

## A. Grammar and terminology

Errors that appear in Caroline's filed samples. Check for each one:

- [ ] "PRILIMINARY" → **PRELIMINARY**
- [ ] "we respectfully prays" → **pray**; "dismissed with costs be paid" → **costs to be paid**
- [ ] "in particularly" → **in particular**
- [ ] "Statement of Claimed" → **Statement of Claim**; "misused of trade secret" → **misuse of**
- [ ] "The said Application as not made bona fide and is clearly tactical manoeuvre" → **was not made *bona fide* and is clearly a tactical manoeuvre**
- [ ] "the D1's …" → **D1's …**
- [ ] Mixed spellings in one document (maneuver/manoeuvre, emphasize/emphasise). Use one throughout, British by default.
- [ ] Singular/plural party labels match the record (Plaintiff vs Plaintiffs; Defendant vs Defendants; "his" vs "her" vs "its" for the deponent/company).
- [ ] Every defined term is defined once, in bold within quotes, before first use, and used verbatim after.
- [ ] In a reply, the "abbreviations adopted" paragraph names **our own** submissions, not the other side's.
- [ ] Missing words where a provision is named mid-sentence ("the said Application for … Order **under** Order 57 Rule 1…").

## B. Numbering and structure

- [ ] Automatic numbering is continuous. No manual "a." mixed with auto "(a)". One sub-level style throughout: (a) → (i).
- [ ] Internal cross-references ("paragraph 14 above") still point to the right paragraph after any insertion. Verify on the rendered PDF: `pdftotext out.pdf - | grep -nE "^\s*[0-9]{1,3}\.\s"`.
- [ ] Heading levels: top = bold underlined caps; argument sub-heading = bold caps (not underlined); third level = bold italic sentence case.
- [ ] CRUX ≤ 3 paragraphs in a reply. Conclusion has the correct prayer for our side (dismiss with costs / order in terms).
- [ ] **No repeated argument.** List each argument once with the paragraph where it is fully made. Any second appearance must be a one-line cross-reference. (The filed E16 submission made the "arbitration would paralyse this action" point at paras 5(g), 42-43 and 48. That is the pattern to avoid.)
- [ ] Empty paragraph between every paragraph; no space-before/after; indentation Left 0 / Right 0 / Hanging 0.5" everywhere.

## C. Citations and record

- [ ] Every case/statute: name + citation fully bold + italic + underlined; Tab number and E-page follow in bold brackets; pin-cite paragraph in italic.
- [ ] Every Tab/E-page checked against the actual BOA (open the page; the quoted paragraph must be on it).
- [ ] Every quotation matches the source word for word; "(emphasis added)" present wherever bold/underline was added.
- [ ] Every factual assertion carries an E-cite that opens to the right page.
- [ ] Every Enclosure number confirmed; unconfirmed ones shown as `[Enclosure ●]` and listed in the delivery note.
- [ ] Case names consistent between first mention and *supra* references; court suffix present.
- [ ] Statute versions noted where amendments matter (check with `malaysian-legislation-library`).
- [ ] Authorities shared with the other side's bundle: decide deliberately whether to cite our tab or theirs, and do it consistently.

## D. Argument strength

- [ ] Each limb of the legal test is answered, and in the order the test sets out.
- [ ] Each of the other side's grounds (from their affidavits and submissions) is answered once, or is deliberately left alone with a reason.
- [ ] No concession by wording: "allegedly", "at most", "even if" used only where intended. Check that "It is not disputed that…" is in fact undisputed on the record.
- [ ] No overstatement of an authority. The proposition attributed to a case must be in the quoted paragraph, not only in the headnote.
- [ ] The other side's own authorities are checked for passages that help us.
- [ ] Any "tactical / abuse" allegation is tied to record facts (dates, parallel applications), not adjectives.
- [ ] New issues in their submissions that are not in any affidavit → Preliminary Objection (statement from the bar).
- [ ] Length: cut any paragraph that does not advance the CRUX.
