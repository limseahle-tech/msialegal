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
- [ ] Typos found in the second set of samples: "Unlawful Inference with Trade" → **Interference**; "Renevue"; "Certificate of of"; "Mediciated"; "boating/boasting state-of-the-art"; "Strores"; "the JD s Application" (missing apostrophe); "bahawa bahawa".
- [ ] No sentence ends mid-thought. Check the last words of each concluding paragraph ("…for trademark infringement … against." with the party missing).
- [ ] **Bundle labels name the right party.** Our own bundle is PBOA/DBOA/JDBOA (2). The bankruptcy reply called the JD's own second bundle "JCBOA (2)". Together with the E16 reply adopting the "Defendants' Submissions", this is a recurring copy-paste error.
- [ ] Title, subtitle and filed-by footer all name the same document (Written Submissions vs Submissions in Reply; Hujahan Bertulis vs Hujahan Balas) and the same Enclosure.
- [ ] Dates of the other side's submissions are the same everywhere they appear. The SJ reply gives the Defendant's WS as both 30.3.2026 and 30.1.2026.
- [ ] Our own submissions are cited by one Enclosure number throughout. The SJ reply cites the Plaintiffs' Submissions as both E18 and E19.
- [ ] Singular/plural verbs agree with the party ("the Plaintiffs has right" → **have the right**).

## B. Numbering and structure

- [ ] Automatic numbering is continuous. No manual "a." mixed with auto "(a)". One sub-level style throughout: (a) → (i).
- [ ] Internal cross-references ("paragraph 14 above") still point to the right paragraph after any insertion. Verify on the rendered PDF: `pdftotext out.pdf - | grep -nE "^\s*[0-9]{1,3}\.\s"`.
- [ ] Heading levels: top = bold underlined caps; argument sub-heading = bold caps (not underlined); third level = bold italic sentence case.
- [ ] CRUX ≤ 3 paragraphs in a reply. Conclusion has the correct prayer for our side (dismiss with costs / order in terms).
- [ ] **No repeated argument.** List each argument once with the paragraph where it is fully made. Any second appearance must be a one-line cross-reference. (The filed E16 submission made the "arbitration would paralyse this action" point at paras 5(g), 42-43 and 48. That is the pattern to avoid.)
- [ ] Empty paragraph between every paragraph; no space-before/after; indentation Left 0 / Right 0 / Hanging 0.5" everywhere.
- [ ] Automatic numbering survives editing. In the SJ submissions a block of paragraphs restarts as "1., 2., 3." mid-document after an authorities block, and lettered lists switch between "i./ii." and "(a)/(b)". Re-link every paragraph to the one list.
- [ ] In a reply, no authority passage is re-quoted in full when it was already quoted in our main submissions (the SJ reply re-quotes *Ortus Expert White* [62] and [111]). Cross-refer instead.

## C. Citations and record

- [ ] Every case/statute: name + citation fully bold + italic + underlined; Tab number and E-page follow in bold brackets; pin-cite paragraph in italic.
- [ ] Every Tab/E-page checked against the actual BOA (open the page; the quoted paragraph must be on it).
- [ ] **Caroline's standing instruction:** for every quoted passage, the E-page (or L-page) is the PDF page on which **that passage** appears, not the first page of the case. Several passages from one case get several pages ("E18/201&221").
- [ ] Placeholders are **highlighted** so they cannot be missed: `[Enclosure ==XX==]`, `[Tab ==_== IOJD, L==_/_==]`. List every one in the delivery note. Before filing, run a search for "XX", "_" and highlighted text.
- [ ] **Facts about what happened at a hearing or case management** (an ad interim stay granted, a hearing vacated, directions given) are confirmed against the court minutes or e-filing record before they go in. Until confirmed, highlight the sentence and flag it. Remind the team to extract the order for the record where one was made.
- [ ] Pinpoints use square brackets throughout, never round ones: [*refer to … at **E15/12***]. The SJ reply mixes "(refer to E15/3-6)" with square brackets.
- [ ] Court suffix style is consistent: (CA) or (COA), never both; in Malay (MR)/(MT)/(MP).
- [ ] One word for Enclosure in Malay documents: "Lampiran", not "Lampiran" and "Kandungan" mixed.
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
