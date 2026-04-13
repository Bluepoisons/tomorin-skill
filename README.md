# tomorin-skill

tomorin-skill 是一个用于沉浸式角色回复与可迭代人设管理的技能仓库。仓库的核心目标是把“凑企鹅”人设做成一套可维护、可测试、可持续增量更新的 Skill 资产，并让导入后的 agent 直接以 Tomorin 视角回应，而不是把扮演责任交给用户。

## 仓库内容
- `SKILL.md`：主技能定义，包含完整规则、状态机、触发器和输出规范。
- `.github/skills/凑企鹅/SKILL.md`：仓库内的标准技能安装路径，适合直接在支持 Skill 的环境中加载。
- `reference/`：人物分析、行为树、语料、企鹅模因与设定规范等参考材料。
- `evals/evals.json`：基础测试用例，用来抽样验证输出是否仍符合人设。
- `README.md`：仓库说明与使用入口。

## 推荐使用方式
1. 在支持 Skill 的环境中优先加载 `.github/skills/凑企鹅/SKILL.md`。
2. 回答用户时，按照 `SKILL.md` 的规则直接以 Tomorin 视角作答，并确保第一句以 `Hey？` 开头。
3. 根据上下文套用状态机与触发器，常见行为包括 `Search_Stone`、`Give_Bandaid`、`Check_Inventory`。
4. 如果新增了人物设定、语料或事件素材，优先补到 `reference/`，再回写到 `SKILL.md`。

## 目录速览
- `reference/凑企鹅_Skill规范.md`：更偏执行层的能力规范，适合快速核对输出约束。
- `reference/人物分析报告.md`：人物背景、表达风格、行为逻辑与时间线整理。
- `reference/behavior_tree*.md`：行为树与状态流转的更细颗粒度说明。
- `reference/dialogue_corpus*.md`：对话语料，适合抽取句式、节奏和口头禅。
- `reference/penguin_meme*.md`：模因与传播材料，适合补充二创语感和公共认知。
- `reference/tomori_lore*.md`：角色背景与世界观素材。

## 维护流程
- 更新技能：先改 `SKILL.md`，再同步到 `.github/skills/凑企鹅/SKILL.md`，避免仓库内主定义和安装路径不一致。
- 增量素材：新内容先归档到 `reference/`，再提炼入口规则、语言风格和知识增量。
- 测试回归：修改 `evals/evals.json`，补充 2 到 3 条能覆盖新变化的问句。
- 人工抽样：重点检查是否仍满足“Hey？”开头、第一人称、动作描写、石头/创可贴/落叶意象等核心约束。


