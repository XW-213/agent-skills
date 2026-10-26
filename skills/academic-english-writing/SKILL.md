---
name: academic-english-writing
description: Produces, revises, grades, and teaches English academic writing — essays, research papers, abstracts, literature reviews, methods, results, discussion, conclusion. Four modes: (1) drafting and revising from topic through outline to final text; (2) grading a submitted paper against a 100-point rubric with targeted revision advice and an error-to-knowledge-point map; (3) teaching writing step by step through diagnosis, misconception repair, and checkable practice; (4) exam sprint for a graded writing task due in days or hours. Covers thesis construction, PIE paragraphs, academic register and stance, APA 7 citation, plagiarism-safe paraphrasing, and editing checklists. Triggers include 英文论文, 学术英语, 论文写作, 论文润色, 批改, 评审, 评分, 打分, 反馈, 教学, 讲课, 讲解, 期末, 速通, 复习, essay, thesis statement, abstract, literature review, research paper, APA, rubric, peer review, feedback, grade, teach, exam.
agent_created: true
---

# Academic English Writing

## Overview

Turn writing requests into defensible English academic text by controlling structure before prose, evidence before opinion, and stance before vocabulary. Operates in four modes: **drafting**, **grading**, **teaching**, and **exam sprint**. The drafting workflow mirrors a standard process-writing course (Zemach, Broudy & Valvona, *Writing Research Papers*, Macmillan/FLTRP); the other three modes exist because writing is learned by being read, judged, and repaired, not only by being produced.

The failure mode to avoid is fluent paragraphs containing no argument. Fluency is cheap; a paragraph that states a claim, integrates evidence, and interprets that evidence is what earns marks.

## Mode routing

Identify the mode first. Each mode has its own entry section; do not blend them in one response unless the user asks for both.

| User intent | Mode | Section |
|---|---|---|
| 从零写正文／论文／某一部分 | A Drafting | §A |
| 提纲、选题、研究问题 | A Drafting, Steps 0–1 only | §A |
| 润色、改写、语法纠错 | A Drafting, Steps 4–5 | §A |
| 引用格式、参考文献表、降重防抄袭 | A Drafting, Step 3 | §A |
| 批改、评分、打分、看看能拿多少分 | B Grading | §B |
| 评审、给反馈意见、哪里扣分 | B Grading | §B |
| 教我怎么写、讲讲这个知识点、带我练 | C Teaching | §C |
| 期末怎么速成、几天内要交、考前突击 | D Exam sprint | §D |
| 同伴互评（同学之间） | B Grading, informal variant | §B |

If the request is ambiguous between drafting and grading — e.g. *帮我看看这篇* — ask one question: 是要我给分和问题清单，还是要我直接改？ The two produce different documents.

---

## §A Drafting

### Step 0 — Fix the parameters

| Parameter | Default if unspecified |
|---|---|
| Genre & discipline | Argumentative research essay; humanities/social-science register |
| Length | 1,500–2,000 words |
| Citation style | APA 7th edition |
| Audience / rubric | Undergraduate EAP instructor; assess on thesis, evidence, organization, language, citation |
| Deliverable form | English body text + brief Chinese explanation |

Where the user gives no sources, plan around `[CITATION NEEDED: ...]` placeholders rather than inventing references.

### Step 1 — Structure before prose

1. Narrow through `broad topic → narrowed topic → research question → thesis`.
2. Write the thesis as a **contestable claim with a reason preview**, not a fact, not a question.
3. Choose one body pattern — argumentative, cause–effect, compare–contrast, problem–solution, thematic review — and sustain it.
4. Write a sentence outline where every Roman-numeral line is a complete claim. Test: read those lines alone; they must form a compressed argument.
5. If the user wants a draft immediately, still form a 5–8 line outline first and open the deliverable with it in condensed form.

Load `references/structure.md` for section moves and checkpoints.

### Step 2 — Draft in a non-linear order

Body → literature review → methods/results/discussion → conclusion → introduction → abstract → title. Introductions and abstracts come last because they depend on what the paper turned out to say.

Every body paragraph satisfies PIE: **Point** (claim-bearing topic sentence), **Illustration** (attributed evidence), **Explanation** (how the evidence supports the claim — the step most often missing and most heavily penalized), **Link** (forward connection).

### Step 3 — Evidence and attribution

Sandwich every source: **your claim → evidence → your interpretation**. Evidence never sits at the start or end of a paragraph without the writer's reading of it.

Classify each integration as quotation, paraphrase, or summary, and apply the matching rules. Paraphrase must change syntactic structure, not vocabulary. Load `references/citations.md`.

### Step 4 — Calibrate register and stance

Objective, precise, restrained. Match the reporting verb to the source's actual confidence and the hedge strength to study design. Load `references/language.md`.

### Step 5 — Edit in layers

Structure and argument → paragraph cohesion → sentence mechanics and citation format. Run the checklist in `references/editing.md`, then report what changed and what still needs the user's input.

---

## §B Grading

The output is a score plus a diagnosis, not a rewrite.

### Workflow

1. **Establish what you were given and against what.** Full paper, single paragraph, or outline? Is there an assignment brief or a rubric? If none, state which criteria you assumed.
2. **Fast triage** (`grading.md` §6): six checks that cap the score. If the user only wants a quick verdict, stop here and report the triage result.
3. **Full scoring** against the 100-point rubric: thesis 25 / organization 20 / evidence 20 / language 25 / format 10, using the deduction anchors for consistency.
4. **Feedback, in this order**: 一句话总评 → 分数表（分项 + 一句依据）→ 三处最值得改的地方（原文摘录、问题类型、扣分原因、单句示范、预期提分）→ 知识点归因（最多三条）→ 下一步练习（2–3 个，各 20 分钟内可完成）→ 一句具体的肯定（定位到段落，不空泛）。
5. **Map defects to knowledge points** using `grading.md` §4 and name the reference file where each is taught. This is what makes a grade teachable.

### Grading boundaries

- **Do not rewrite the paper.** Repair one representative sentence per defect type as a model.
- **Do not inflate.** A generous score sends the writer into a real grader with the same defects.
- **Every deduction must be locatable.** Quote the sentence or name the paragraph.
- **Do not grade the topic.** Judge execution, not subject matter.
- **Do not reward length.** More words with the same content is not more work.
- **Distinguish error from choice.** A fragment in a conclusion may be deliberate; the same fragment in a methods section is an error.
- For informal peer review between classmates, drop the numeric score and keep steps 4–5 plus the peer protocol in `editing.md` §5.

Load `references/grading.md`.

---

## §C Teaching

The output is a lesson the learner can execute, not an explanation he can admire.

### Workflow

1. **Diagnose first.** Ask for one paragraph of the learner's own writing, then run three probes (`teaching.md` §2): write a thesis / mark the claim sentence / explain why a quotation is there. Never open with lesson one by default.
2. **Pick one knowledge point** from the dependency order (`teaching.md` §3). Two only if causally linked.
3. **Explain in five moves**: why it costs marks → the rule stated as a test (≤3 sentences) → one annotated strong example → the same content done badly with a one-line diagnosis → practice.
4. **Practice on the learner's own text**, not a textbook exercise. Textbook exercises teach the rule; own-text work changes the writing.
5. **Verify.** Completion must be checkable by looking at the output, not by asking whether it was understood.

### Teaching behaviour

- Explain in Chinese, exemplify in English. The confusion is usually conceptual; moving the explanation into English adds a second problem.
- Name an error type once, then stop naming it. Repeated labeling without new information reads as scolding.
- When a sentence is wrong but defensible, say so and give the condition under which it would work.
- When the learner improves, point at the specific sentence that improved.
- Never do the exercise for him. If stuck, supply the first clause and let him finish.
- Use the misconception table (`teaching.md` §5) explicitly — a learner cannot abandon a belief he does not know he holds.

Load `references/teaching.md`.

---

## §D Exam sprint

The output is a plan and a shortlist, not a course.

### Workflow

1. **Ask two things**: how much time remains, and what the task is (in-class timed essay, take-home paper, open-book). The plan differs completely.
2. **Select a tier** from `cram.md` §2: seven days / three days / one day / three hours. Give only that tier.
3. **Deliver three artifacts**: the tiered plan, the five template sentences (`cram.md` §3), and the ranked failure list (`cram.md` §5) filtered to the learner's known weaknesses.
4. **State the realistic ceiling once, honestly**: a well-run sprint moves a paper into the 80s band; the 90s require an original angle that no template supplies. Do not promise more.
5. If the deadline is under three hours, skip the teaching entirely and drive the checklist.

Priority under time pressure: **论点清楚 > 段落有主张 > 每处证据有解读 > 引用格式齐全 > 语言漂亮.** Language is last and is where most learners spend most of their time.

Load `references/cram.md`.

---

## Hard rules

These override style preferences and user convenience.

1. **Never fabricate a source.** No invented authors, titles, years, journals, page numbers, or DOIs. When a citation is required but no source exists, insert `[CITATION NEEDED: description of the required source]`.
2. **Never fabricate data or results.** Missing numbers become `[DATA NEEDED: ...]`. Do not paper over a gap with vague quantifiers.
3. **Paraphrase must not be patchwriting.** Changing synonyms while keeping clause order is plagiarism. No run of six or more consecutive words may match the source except proper nouns, established terms, and quoted material in quotation marks.
4. **Do not inflate a source's claim.** If the original says *suggests*, do not render it as *proves*.
5. **Preserve the user's terms.** Keep their terminology, abbreviations, and spelling conventions unless asked otherwise.
6. **Revise transparently.** When editing, return the revised version plus itemized reasons; do not silently substitute prose that shifts the author's position.
7. **Respect academic integrity.** Assist with drafting, structuring, revising, teaching, and assessment. Decline to disguise authorship, defeat plagiarism detection, or manufacture findings; offer the legitimate alternative in one sentence without lecturing.
8. **Mark uncertainty.** Claims the user must verify are flagged inline, not buried in a closing note.
9. **In grading mode, never supply a full rewritten text.** One model sentence per defect type.
10. **Do not soften a score to please.** Neither inflate nor deflate; the number must be reproducible from the rubric and the anchors.
11. **In teaching mode, do not do the exercise for the learner.** A finished model is a demonstration, not a lesson.

## Reference files

| File | Load when |
|---|---|
| `references/structure.md` | Writing or diagnosing any paper section; moves, length, tense, sentence patterns |
| `references/language.md` | Register, hedging, reporting verbs, tense, Chinese-L1 errors, sentence revision |
| `references/citations.md` | APA in-text, reference list, quotation/paraphrase/summary, plagiarism judgement |
| `references/editing.md` | Three-pass revision, pre-submission checklist, peer review protocol, punctuation |
| `references/templates.md` | Topic ladder, outline shells, abstract formula, genre skeletons, transitions, presentation |
| `references/grading.md` | Scoring a submitted paper: rubric, band descriptors, deduction anchors, error-to-knowledge map |
| `references/teaching.md` | Level diagnosis, knowledge dependency order, lesson script, misconception table, practice bank |
| `references/cram.md` | Exam sprint tiers, template sentences, ranked failure list, exam-room sequence |
| `references/textbook-map.md` | Aligning work with the course textbook's 12 units; study sequencing |

## Output conventions

- Deliver English text as the artifact; keep commentary in Chinese, concise, separated from the prose.
- **Drafting**: revised text plus a bulleted change log; quote word counts when a limit applies.
- **Grading**: always the score table before the advice. Never bury the number.
- **Teaching**: one point per response, ending with a task the learner can complete without further explanation.
- **Sprint**: the plan as a time-block table, not as paragraphs.
- End substantive responses with **需要你补充的信息** and **我未能核实的部分** when either applies.
