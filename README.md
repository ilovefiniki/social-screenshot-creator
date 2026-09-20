# 📸 Social Screenshot Creator

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![Python 3.10+](https://img.shields.io/badge/python-3.10+-blue.svg)](https://www.python.org/)
[![Playwright](https://img.shields.io/badge/Playwright-Chromium-45ba4b.svg)](https://playwright.dev/)
[![Compatible with AI Agents](https://img.shields.io/badge/AI%20Agents-Claude%20%7C%20Antigravity%20%7C%20Cursor-black)](#)

Generate realistic, pixel-perfect 2x Retina screenshots of social media posts across **LinkedIn**, **Threads**, and **X (Twitter)** from plain text in a single command.

Eliminates manual screenshotting, Figma mockups, and paid visual APIs. Perfect for tech blogs, newsletters, and social marketing workflows.

Part of the **[ILF Studio](https://ilf-studio.com)** & **[ilovefiniki.com](https://ilovefiniki.com)** AI engineering toolset.

---

## ⚡ Quickstart

### 1. Installation
```bash
git clone https://github.com/ilovefiniki/social-screenshot-creator.git
cd social-screenshot-creator
pip install playwright pillow
playwright install chromium
```

### 2. Generate Screenshots
```bash
python3 scripts/generate_screenshot.py \
  --text "AI-native engineering means shifting from prompt-tuning to deterministic governance loops."
```

Output directory: `./screenshots/YYYY-MM-DD_slug/`
- `linkedin_post.png` — LinkedIn Light theme card
- `threads_post.png` — Threads Dark theme card
- `x_post.png` — X.com Black theme card

---

## 🎨 Features

- **Multi-Platform in One Pass:** Generates synchronized visual cards for LinkedIn, Threads, and X.
- **2x Retina Crispness:** Rendered at high DPI via Playwright headless browser.
- **Thread & Comment Support:** Add `--comment "your link"` to render connected reply cards.
- **Neutral Defaults / Fully Customizable:** Comes with a built-in clean avatar and neutral persona (`Alex Rivers`), but easily accepts your own `--name`, `--handle`, and `--avatar`.
- **Dialogue Sticker Generator:** Includes `scripts/generate_stickers.py` to create side-by-side conversational sticker cards.

---

## 🛠️ CLI Flags & Options

```bash
python3 scripts/generate_screenshot.py \
  --text "Your text" \
  --comment "Optional reply" \
  --name "Your Name" \
  --handle "yourhandle" \
  --title "Your Headline" \
  --avatar "path/to/avatar.jpg" \
  --output-dir "./output"
```

| Argument | Default | Description |
|---|---|---|
| `--text` | *(Required)* | Full post body. |
| `--comment` | `None` | Optional comment card. |
| `--name` | `Alex Rivers` | Author name. |
| `--handle` | `alexrivers` | Social handle. |
| `--title` | `AI Engineer & Systems Architect` | Bio / Headline. |
| `--avatar` | `assets/default_avatar.png` | Path to author avatar. |
| `--output-dir`| `./screenshots` | Target folder. |

---

## 🤖 Use as an AI Agent Skill

Install directly into your agent workspace:

```bash
# Antigravity & Gemini:
mkdir -p .agents/skills/social-screenshot-creator && curl -fsSL https://raw.githubusercontent.com/ilovefiniki/social-screenshot-creator/main/SKILL.md -o .agents/skills/social-screenshot-creator/SKILL.md

# Claude Code:
mkdir -p .claude/skills/social-screenshot-creator && curl -fsSL https://raw.githubusercontent.com/ilovefiniki/social-screenshot-creator/main/SKILL.md -o .claude/skills/social-screenshot-creator/SKILL.md
```

---

## 📄 License

Released under the [MIT License](LICENSE). Maintained by [Vitaliy Alhimovich](https://github.com/ilovefiniki) at [ILF Studio](https://ilf-studio.com).
