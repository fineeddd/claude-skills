# claude-skills

Claude Code 自定义 Skills 合集 / Custom Skills for Claude Code

---

## Skills 列表 / Skill List

| Skill | 语言 | 说明 |
|-------|------|------|
| [systematic-learning](./systematic-learning/) | 中文 | 系统化课程与书籍学习教练 |
| [systematic-learning-en](./systematic-learning-en/) | English | Systematic course & book learning coach |

---

## 安装方法 / Installation

每个 Skill 目录下有独立的 README，包含安装命令。

Each skill directory has its own README with installation instructions.

**快速安装 / Quick install:**

```bash
# 中文版
mkdir -p ~/.claude/skills/systematic-learning
curl -o ~/.claude/skills/systematic-learning/SKILL.md \
  https://raw.githubusercontent.com/fineeddd/claude-skills/main/systematic-learning/SKILL.md

# English version
mkdir -p ~/.claude/skills/systematic-learning-en
curl -o ~/.claude/skills/systematic-learning-en/SKILL.md \
  https://raw.githubusercontent.com/fineeddd/claude-skills/main/systematic-learning-en/SKILL.md
```

---

## 关于 Claude Code Skills / About Claude Code Skills

Skills 是放在 `~/.claude/skills/<skill-name>/SKILL.md` 的 Markdown 文件，Claude Code 会在合适的时机自动加载并触发。

Skills are Markdown files placed at `~/.claude/skills/<skill-name>/SKILL.md`. Claude Code automatically loads and triggers them at the right moment.

了解更多 / Learn more: [Claude Code Documentation](https://docs.anthropic.com/claude/claude-code)
