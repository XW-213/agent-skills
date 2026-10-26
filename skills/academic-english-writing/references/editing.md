# Editing, Checking, and Peer Review

Reference for layered revision, the pre-submission checklist, the peer review protocol, and the diagnostic script for judging a draft.

---

## 1. Why layered revision

Editing everything simultaneously produces local polish on top of structural failure: flawless sentences arranged in an argument that does not hold. Fix in three passes, in order, because a later pass is wasted if an earlier one changes the text.

| Pass | Scope | Technique | Effort share |
|---|---|---|---|
| 1 | Argument and structure | Print it. Read only the thesis, then only the topic sentences, then only the first and last sentence of each paragraph | 50% |
| 2 | Paragraph and cohesion | Check each paragraph for Point–Illustration–Explanation–Link; check that sentence N+1 begins where sentence N ended | 30% |
| 3 | Sentence and mechanics | Read aloud; then read backwards sentence by sentence; then check citation format and reference list | 20% |

Rationale for backwards reading: it removes narrative momentum, so agreement, article, tense, and spelling errors surface instead of being auto-corrected by the reading brain.

---

## 2. Pass 1 — structural audit

Answer each question with a line number or "no".

1. Is the thesis a contestable claim rather than a fact or a question?
2. Does the thesis preview the reasons the body will develop?
3. Do the topic sentences, read in isolation, form a coherent argument?
4. Does any paragraph fail to serve the thesis? If so, cut or relocate it.
5. Does each paragraph contain at least one piece of evidence?
6. Does each piece of evidence have an interpretation attached?
7. Is the counterargument, if the genre needs one, the strongest available version rather than a straw man?
8. Does the conclusion avoid new evidence and new claims?
9. Does the conclusion's scope match the evidence and sample?
10. Does the introduction's gap statement match the gap the paper actually fills?

Output of Pass 1: a numbered defect list ordered by severity. Resist correcting grammar until this list is empty.

---

## 3. Pass 2 — paragraph audit

Per paragraph:

- **Point**: is the topic sentence a claim, not a label? *Automated feedback is widely used* is a fact; *Automated feedback improves accuracy but not fluency* is a claim.
- **Illustration**: is the source identified, and is the evidence actually evidence for this claim rather than merely on the same topic?
- **Explanation**: is there a sentence beginning with something like *This suggests that* or *One reason for this is*? Its absence is the single most common defect.
- **Link**: does the paragraph end by connecting forward, not with a quotation?
- **Length**: 5–10 sentences. Over 12, split. Under 4, either merge or develop.
- **Unity**: any sentence that could be moved to another paragraph without loss signals a unity problem in this one.

Paragraph transitions should be carried by content, not by a decorative connective. If two paragraphs are genuinely related, restating the shared term in the second paragraph's first clause does more than inserting *Furthermore*.

---

## 4. Pre-submission checklist

Use verbatim. Items 1–10 are structural and cost the most; 11–20 are mechanical.

- [ ] 1. Title states object and approach, 10–15 words, no terminal period.
- [ ] 2. Abstract contains background, method, findings with specifics, interpretation, and boundary — and nothing absent from the body.
- [ ] 3. Thesis is contestable and appears in the introduction.
- [ ] 4. Every topic sentence serves the thesis.
- [ ] 5. Every paragraph has evidence-to-interpretation pairing.
- [ ] 6. The strongest counterargument is represented and answered (if the genre requires it).
- [ ] 7. Conclusion introduces no new evidence and no new source.
- [ ] 8. Conclusion's claims stay inside the sample's reach.
- [ ] 9. Section order and headings follow the required template.
- [ ] 10. Word count within ±10% of the requirement.
- [ ] 11. In-text citations and reference entries match one for one, both in count and in spelling.
- [ ] 12. Reference list alphabetical, hanging indent, consistent style, DOIs as full links.
- [ ] 13. Every direct quotation has quotation marks and a page number.
- [ ] 14. No paraphrase retains the source's sentence structure.
- [ ] 15. Tense follows the section rules: method and results past, interpretation present, author claims present.
- [ ] 16. No *very*, *really*, *a lot of*, *etc.*, *and so on*.
- [ ] 17. Every abbreviation defined at first mention.
- [ ] 18. No comma splices, no run-ons (verified by reading aloud).
- [ ] 19. Numbers follow APA: words below 10, numerals 10 and above, no sentence begins with a numeral.
- [ ] 20. No Chinese full-width punctuation anywhere in the English text.

---

## 5. Peer review protocol

Purpose: help the author see what the text actually says, as distinct from what the author intended.

**Sequence**
1. Read once without marking, to state the paper's argument back to the author in one sentence. If you cannot, that is the first finding — a clarity defect in the thesis or the topic sentences.
2. Second read, marking only two categories: places where you were convinced, and places where you were not.
3. For each unconvincing place, name the missing element: claim unclear, evidence absent, evidence irrelevant, interpretation missing, logical leap.
4. Rank findings by severity: structure > evidence > cohesion > language.
5. Give at least one specific strength, located by line, not as a courtesy but as information about what to preserve.

**Feedback quality rule**
- Unusable: *This paragraph is weak.*
- Usable: *In paragraph 3, you cite Li (2020) but never say how the finding supports your claim that feedback quality matters more than frequency. Two sentences of analysis after the citation would fix it.*

**Do not** rewrite the author's sentences in peer review. Rewriting transfers ownership and hides the underlying problem. Point at the defect and let the author solve it.

---

## 6. Diagnostic script for judging an unfamiliar draft

When a user submits a draft and asks what is wrong, run this and report the findings as a ranked list.

1. Locate the thesis. If it takes more than fifteen seconds, mark "thesis not retrievable".
2. Extract all topic sentences into a list. Check whether they form an argument or a list of topics.
3. Count paragraphs without evidence; count paragraphs without interpretation.
4. Check whether the conclusion's claim is stronger than the strongest piece of evidence.
5. Check the citation apparatus: count in-text citations, count reference entries, compare.
6. Sample three paraphrases; compare each against its source if the source is available, or check for structural mirroring if it is not.
7. Scan for the Chinese-L1 error inventory in `language.md` §7.
8. Report: structural defects first, with line references; then language issues grouped by type rather than listed one by one.

---

## 7. Common punctuation and mechanics errors

| Error | Wrong | Right |
|---|---|---|
| Comma splice | *The results were significant, we rejected the hypothesis.* | *The results were significant; we therefore rejected the hypothesis.* |
| Run-on | *AI feedback is useful it saves time and it is objective.* | Split into two or three sentences |
| Missing serial comma | *accuracy, fluency and complexity* | *accuracy, fluency, and complexity* |
| Spaced em dash | *the result — which was expected — surprised us* | *the result—which was expected—surprised us* |
| Hyphen after the noun | *a well-designed study* / *the study was well-designed* | *the study was well designed* |
| Full-width punctuation | *写作，research。* | Use ASCII punctuation throughout English text |
| Apostrophe in plural | *the 1990's* | *the 1990s* |
| *i.e.* for *e.g.* | *tools, i.e. Grammarly* | *tools, e.g. Grammarly* |
| Double space after period | — | Single space |
| Quotation mark placement | *“...”.* | *“....”* |
