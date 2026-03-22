# 📚 Systematic Learning — Claude Code Skill (English)

A **systematic course and book learning coach** Skill designed for Claude Code.

Provide a file path, and Claude reads the content automatically, guiding you through a complete learning journey: learner profiling → roadmap → chapter-by-chapter study → Feynman verification → review loop. All outputs are saved as local Markdown files.

> 中文版请见 [systematic-learning](../systematic-learning/)

---

## Features

- **Reads local files directly**: supports PDF, TXT, MD, or entire directories — no knowledge base needed
- **Adaptive to course type**: auto-detects Practical / Conceptual / Critical and adjusts questioning strategy
- **Learner profiling**: 3–5 rounds of conversation to understand background, motivation, and skill level
- **Precise roadmap**: organized by stage, precise to each individual chapter, with 🔴/🟡/⚪ study depth markers
- **Chapter-by-chapter coaching**: overview + block-by-block teaching (explain → connect → check-in), tailored to your background
- **Feynman verification**: you explain it first, Claude probes, surfaces gaps between "thinking you understood" and actual understanding
- **Stage review loop**: mastery audit + closure decision (re-study / practice / advance)
- **Auto file saving**: roadmap, study notes, verification logs saved as local MD files

---

## Installation

### Option 1: Manual install

```bash
mkdir -p ~/.claude/skills/systematic-learning-en
curl -o ~/.claude/skills/systematic-learning-en/SKILL.md \
  https://raw.githubusercontent.com/fineeddd/claude-skills/main/systematic-learning-en/SKILL.md
```

### Option 2: Clone the repo

```bash
git clone https://github.com/fineeddd/claude-skills.git
cp -r claude-skills/systematic-learning-en ~/.claude/skills/
```

---

## Usage

In Claude Code, simply tell Claude you want to study a course and provide the file path:

```
Help me systematically study /path/to/your/course
```

**Trigger phrases:**
- `Help me systematically study [file path]`
- `I want to learn this book step by step: [file path]`
- `Use a learning framework to help me study [file path]`
- `Walk me through this course: [file path]`

**Supported file types:**
- Single files: `.txt`, `.md`, `.pdf`
- Directories: folders containing multiple course files

---

## Learning Flow

```
Start → Claude reads files
       ↓
Step 1  Understand you (3–5 rounds) → Learner profile
       ↓
Step 2  Course structure analysis → Author's logic + goal mapping
       ↓
Step 3  Generate learning roadmap → By stage, chapter-precise
       ↓
  ┌─── Learning loop (repeat per chapter) ──────────────┐
  │  4a Chapter overview                                 │
  │  4b Block-by-block teaching                         │
  │  4c Chapter closing summary                         │
  │  5b Feynman verification (ongoing)                  │
  │  End of stage → 5a Stage verification               │
  │  Step 6  Review & closure                           │
  └──────────────────────────────────────────────────────┘
```

**Generated files** (saved in `learning-records/` next to your course files):

| File | Contents |
|------|----------|
| `01_learner-profile.md` | Knowledge map, core motivation, learning preferences |
| `02_course-structure-analysis.md` | Value assessment, module dependencies, completeness check |
| `03_learning-roadmap.md` | Staged roadmap (mastery status updated as you progress) |
| `04_study-notes.md` | Chapter-by-chapter notes (appended continuously) |
| `05_verification-log.md` | Feynman and stage verification records |

---

## Best For

- Systematically studying paid course transcripts
- Deep-reading a book in digital format
- Processing a batch of learning materials (articles, notes, lecture slides)

---

## License

MIT
