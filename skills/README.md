# skills — 技能索引

`skill` 分支是三条领域线的集成点。三个领域分支从这里拉出，独立演进；只有验证过能用的技能才并回这里。

`skill` is the integration point for the three domain lines. Each domain branch is cut from this one and evolves independently; only skills that have been proven to work are merged back.

## 分支 / Branch map

| 分支 | 领域 | 技能 | 状态 |
|---|---|---|---|
| `skill-education` | 教育 | `academic-english-writing` | 可用 |
| `skill-security` | 网络安全 | — | 规划中 |
| `skill-development` | 后端开发 | — | 规划中 |

```
skill
├── skill-education      → skills/academic-english-writing/
├── skill-security       → skills/<security 技能>/
└── skill-development    → skills/<开发技能>/
```

> 分支名用连字符而非斜杠：Git 不允许 `skill` 与 `skill/education` 并存（ref 路径冲突：一个要当文件，一个要当目录）。

## 一个技能长什么样

```
skills/<skill-name>/
├── SKILL.md          必需。YAML frontmatter（name / description / agent_created）+ 主流程
├── README.md         建议。给不熟悉这个技能的人看的说明
└── references/       可选。按需加载的细节，保证 SKILL.md 保持精简
```

三条约定：

1. **目录名必须等于 `SKILL.md` 里 `name` 字段的值**，否则部分平台识别不到。
2. **`description` 写"什么时候用"**，不是"这是什么"。agent 靠它决定要不要加载这个技能。
3. **主文件控制在 2000 词以内**，把细节推到 `references/`，用表格告诉 agent 何时加载哪一份。

## 新增一个技能

```bash
git checkout skill-education        # 或 skill-security / skill-development
mkdir -p skills/<new-skill>/references
# 写 SKILL.md，校验后再提交
git add skills/<new-skill>
git commit -m "feat(<domain>): add <new-skill>"
```
