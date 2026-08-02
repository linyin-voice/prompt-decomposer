# 🎨 Image Prompt Decomposer / 图片提示词拆解器

A browser-based AI tool that analyzes images and generates detailed, categorized prompts for AI image generation.

## Features

- **10 Analysis Categories**: Art Style, Character, Clothing, Action, Background, Lighting, Color, Composition, Atmosphere, Details
- **3 Detail Modes**: Simple, Complex, Ultra-Detailed — with per-category granularity control
- **2 Style Modes**: Precise (literal) and Fuzzy (evocative) prompt generation
- **Batch Processing**: Upload multiple images for sequential analysis with progress tracking
- **History System**: Auto-saved results with search and restore (IndexedDB)
- **Prompt Templates**: Stable Diffusion, Midjourney, and NovelAI format output
- **Multi-format Export**: TXT, Markdown, JSON
- **Negative Prompts**: Auto-generated negative prompt for each image
- **Inline Editing**: Click any result to edit directly
- **Dark/Light Theme**: Toggle between themes
- **Safety Filter**: Optional NSFW/content blocking
- **Chinese/English**: Full i18n for UI and AI output language

## How to Use

1. Open `index.html` in a browser (serve via any static server, or deploy to GitHub Pages)
2. Enter your API Key (SiliconFlow or any OpenAI-compatible API)
3. Upload an image
4. Click "Generate Prompts"
5. Copy, edit, or export the results

### API Configuration

Default API: **SiliconFlow** (`Qwen/Qwen3-VL-8B-Instruct`)

Each user enters their own API key (stored locally in browser localStorage). Get a key at [siliconflow.cn](https://siliconflow.cn).

## Deployment

### GitHub Pages (Free)

1. Fork or push this repo to GitHub
2. Go to Settings → Pages → Source: Deploy from a branch → Select `main` → Save
3. Your site will be live at `https://your-username.github.io/repo-name/`

### Local Development

```bash
cd d:\photos
python -m http.server 8080
# Open http://localhost:8080
```

## Tech

- Single-file HTML/CSS/JS (no build step, no dependencies)
- OpenAI-compatible API format for vision LLM calls
- IndexedDB for history storage
- localStorage for settings persistence
