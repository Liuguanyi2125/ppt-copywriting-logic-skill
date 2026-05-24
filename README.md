# PPT 文案逻辑梳理 Skill

一个 Codex / Claude skill，用来把原始材料梳理成 PPT 页面级结论、文案层级、逻辑关系、页面结构，以及可选的 AI 视觉提示词。

核心顺序：

```text
页面任务 -> 信息颗粒 -> 信息关系 -> 页面级结论 -> PPT 文案层级 -> 页面结构 -> 可选 AI 视觉提示词
```

## 适合什么场景

- 把会议纪要、方案材料、论文内容、领导给的散乱信息整理成 PPT 页面文案。
- 判断一页 PPT 为什么逻辑乱、标题弱、信息关系看不清。
- 把长段文字压缩成可读的页面标题、二级要点和备注信息。
- 在 AI 美化或生成 PPT 之前，先明确页面任务、内容主线和版式结构。

## 安装到 Codex

```bash
mkdir -p ~/.codex/skills
git clone https://github.com/Liuguanyi2125/ppt-copywriting-logic-skill.git ~/.codex/skills/PPT\ 文案逻辑梳理
```

重启 Codex，或刷新 skill 列表后，使用下面这类表达触发：

```text
用 PPT 文案逻辑梳理 skill，帮我把这段材料整理成一页 PPT
这页 PPT 逻辑怎么排？
帮我梳理 PPT 文案和页面结构
```

## 安装到 Claude Code

```bash
mkdir -p ~/.claude/skills
git clone https://github.com/Liuguanyi2125/ppt-copywriting-logic-skill.git ~/.claude/skills/PPT\ 文案逻辑梳理
```

## 使用方式

把原始材料直接贴给模型，然后说：

```text
请用「PPT 文案逻辑梳理」skill 处理：

【受众】
老板 / 客户 / 学生 / 评委

【用途】
汇报 / 答辩 / 销售 / 培训 / 复盘

【原始材料】
...
```

如果只想练习，可以说：

```text
带我练 PPT 文案逻辑梳理，我只想做选择题。
```

## 输出内容

默认会输出：

- 页面任务
- 信息颗粒
- 逻辑关系
- 页面级标题
- PPT 文案层级
- 页面结构建议
- 可以删掉的信息
- 下一步动作

只有你明确要求「给 AI 提示词」或「顺便生成视觉提示词」时，才会追加 AI 视觉提示词。

## 许可

本项目使用 MIT License。
