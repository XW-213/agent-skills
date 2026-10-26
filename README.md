# agent-skills

> 按领域划分的 AI agent 技能库 · Skills for AI agents, organized by domain.

这个仓库存放可以直接装进 agent 的技能包（skill）。每个技能是一份 `SKILL.md` 加若干按需加载的参考资料，描述"在什么情况下按什么流程做某类任务"，让 agent 从通用助手变成某个领域里靠得住的手。

This repo holds installable skills for AI agents. Each skill is one `SKILL.md` plus on-demand reference files: a description of *when* and *how* to perform a class of tasks, which turns a general assistant into a dependable practitioner of one domain.

---

## 分支结构 / Branches

| 分支 | 领域 | 当前状态 |
|---|---|---|
| `main` | 仓库骨架、说明、许可证 | 已完成 |
| `skill` | 技能分支的集成线，放总索引 | 已完成 |
| `skill-education` | 教育：学术英语写作 | **已有技能** `academic-english-writing` |
| `skill-security` | 安全：网络空间安全 | 待建设 |
| `skill-development` | 开发：后端工程 | 待建设 |

三个领域分支从 `skill` 拉出，各自独立演进；`skill` 只合并已经验证可用的技能。这样一条线上的技能坏了，不会连带影响另外两门。

分支名用连字符而不是斜杠，是 Git 的限制：它不允许同时存在 `skill` 和 `skill/education` 两个 ref（一个要当文件、一个要当目录，路径冲突）。`skill-education` 这种写法在 GitHub 的分支列表里同样按字母成组显示，效果一样，但不会和父分支打架。

---

## 教育线：academic-english-writing

一个用于英文学术写作的技能，覆盖**写、评、教、考**四种场景。

| 模式 | 触发场景 | 产出 |
|---|---|---|
| **A 写作** | 从零写论文／essay，或写其中某一节 | 英文正文 + 中文改稿说明 |
| **B 批改** | 把写好的文章丢进来，问能拿多少分 | 五维分数表 + 三处改进 + 知识点归因 |
| **C 教学** | 想搞懂某个知识点，或需要人带着练 | 诊断结果 + 单点讲解 + 可检验的练习 |
| **D 速通** | 几天内要交，考前突击 | 按剩余时间倒排的计划 + 保命句型 + 失分点清单 |

### 它凭什么可信

不是"又一个写作提示词"。它的结构来自一本真实的课程教材——外研社引进版《学术英语论文写作》（*Writing Research Papers*, Zemach / Broudy / Valvona, Macmillan Writing Series L4）的 12 个单元；批改用的是一张 100 分量表，每一项扣分都要求能定位到具体句子，同一个学生交两次分数不会差 10 分。

实测：用它生成的一篇 200 词课程 essay，在学习通 AI 评审中拿到 100/100。**这是单例，不代表普遍水平**——它说明这套结构在标准化评分下站得住，但没法证明每篇都能满分。

### 它刻意不做的事

- 不编造文献、页码、DOI。缺来源就留 `[CITATION NEEDED]`，缺数据就留 `[DATA NEEDED]`。
- 不把改写写成"换同义词"。连续六个词与原文相同即视为抄袭。
- 不放大原文立场。原文说 *suggests*，不许写成 *proves*。
- 批改模式下不给全文重写，只给每种错误一句示范。
- 不为了让用户高兴而抬分。

### 文件构成

```
skills/academic-english-writing/
├── SKILL.md              主流程：模式路由 + 四个模式 + 11 条硬规则
├── README.md             这个技能的详细说明
└── references/
    ├── structure.md      各章写作动作、篇幅、时态、句式、失分点
    ├── language.md       语体、hedging、引述动词、时态、中式英语纠错
    ├── citations.md      APA 7 文内引用与条目、改写流程、抄袭判定
    ├── editing.md        三遍修改法、20 项清单、互评协议
    ├── templates.md      选题阶梯、提纲外壳、摘要公式、五种文体骨架
    ├── grading.md        100 分量表、扣分锚点、反馈六段式、错误归因表
    ├── teaching.md       水平诊断、知识依赖顺序、讲解脚本、误解清单
    ├── cram.md           速通四档计划、五句保命句型、考场流程
    └── textbook-map.md   教材 12 单元与本技能的映射
```

设计上刻意把主文件压到 1800 词以内：`SKILL.md` 只放流程和硬规则，细节全在 `references/`，按需加载。这样技能被调用时不占满上下文。

---

## 安装 / Installation

**方式一：手工放置**

把 `skills/academic-english-writing/` 整个文件夹复制到：

```
~/.workbuddy/skills/            # 用户级，所有项目可用
<repo>/.workbuddy/skills/       # 项目级，仅当前项目
```

重启 agent 或新开一个会话即可被发现。

**方式二：打成 zip 后导入**

```bash
zip -r academic-english-writing.zip academic-english-writing/
```

把 zip 交给技能的导入入口。注意导入器要的是**压缩包或文件夹**，不是单个 `.md` 文件——单文件会报"没有找到 SKILL.md"。

---

## 设计原则 / Design principles

三条贯穿全库的规矩，后续安全线和开发线的技能也会遵守：

1. **可验证优先于好听。** 分数要能从量表推出来，结论要能指回证据，练习要能看出做没做到。
2. **流程写在主文件，知识写在参考文件。** 主文件是给 agent 的执行路径，不是教科书。
3. **不假装能做的事。** 缺资料就说缺，做不到就说做不到，不给"大概也许可以"的答案。

---

## 许可 / License

[CC BY 4.0](LICENSE) — 可以自由使用、修改、商用，保留署名即可。

---

## English

**agent-skills** is a repository of installable skills for AI agents, organized by domain branches: `skill-education`, `skill-security`, `skill-development`, all cut from the integration branch `skill`.

The first completed skill is **`academic-english-writing`**, which operates in four modes:

- **Drafting** — from topic narrowing and thesis construction through outline, section-by-section drafting, APA citation, and layered editing.
- **Grading** — a 100-point rubric across thesis (25), organization (20), evidence and reasoning (20), language (25), and format (10), with every deduction traceable to a specific sentence, plus an error-to-knowledge-point map so the grade is teachable.
- **Teaching** — level diagnosis through three probes, one knowledge point per session, a five-step lesson script, and practice that can be verified rather than merely understood.
- **Exam sprint** — tiered plans for seven days, three days, one day, or three hours, built on the observation that nine of the ten most costly failures are structural rather than lexical.

The structural framework follows *Writing Research Papers* (Zemach, Broudy & Valvona, Macmillan Writing Series L4) and the operational rules are calibrated to APA 7th edition.

Hard constraints: no fabricated sources or data; paraphrase must change syntactic structure, not vocabulary; source claims are never inflated; grading never rewrites the paper and never softens a score to please.

Licensed under CC BY 4.0.
