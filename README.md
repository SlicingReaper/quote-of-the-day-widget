# “ QUOTE//DAY — a quote a day

![macOS](https://img.shields.io/badge/macOS-Übersicht-3ef0ff?style=flat-square&logo=apple&logoColor=white&labelColor=040914) ![Vibecoded](https://img.shields.io/badge/vibecoded-with%20Claude-ff5ad9?style=flat-square&labelColor=040914)

A new quote every night at midnight, drawn from a built-in pool of **300**: 200 Bible verses (KJV, public domain) and 100 quotes from Stoics, athletes, writers and leaders. Rate them and the draw adapts; add your own and they join the pool.

| File | What |
|:--|:--|
| `quote.jsx` | The widget (230 × 176, under STUDY//TERM by default) |
| `quote.py` | Backend: daily draw, ratings, your quotes |
| `quotes.json` | The pool, copied to your data folder on first install (edit freely) |

## Use it

- **⚙** (top right) opens QUOTE//CFG:
  - **▲ LIKE**: this quote is drawn ×1.2 as often. **▼ DISLIKE**: ×0.8. Same button again clears it; the other button switches.
  - **+ ADD QUOTE**: quote, author or verse, and a † box for scripture → SAVE.
- Bible verses show **†** and the reference; others show author and source / year.

## How the draw works

The first refresh after midnight draws the day's quote and saves it, so it stays put all day. The draw is weighted random (liked ×1.2, disliked ×0.8, everything else ×1.0). Anything shown in the last 150 days is skipped, so the whole pool comes round before anything repeats.

## Data

`~/Library/Application Support/STUDYTERM/standalone/data/`
- `quotes.json`: the pool. Keep `id`s stable so your ratings stay attached. Reinstalling never overwrites it.
- `quotes-user.json`: your likes and dislikes, your own quotes, and the day-by-day history

Want a different pool? Replace `quotes.json` with your own in the same format: `{"quotes": [{"id", "text", "by", "src", "ref", "xian"}]}`.

## 🚀 Install

1. Download this repo (green **Code** button → *Download ZIP*) and double-click **`install.command`**. The first time, macOS may block it: right-click → *Open*.
   It installs [Übersicht](https://tracesof.net/uebersicht/) if you don't have it and copies `quote.jsx` into its widgets folder, plus `quote.py` into `~/Library/Application Support/STUDYTERM/standalone/bin/`.
2. Click the widget to use it. If clicks fall through to the desktop: Übersicht menu-bar icon → this widget → turn on interaction.

- **Needs:** macOS 13+ · `python3` 3.8+ (run `xcode-select --install` if you don't have it)
- **By hand:** Copy `quote.jsx` into Übersicht's widgets folder (menu-bar icon → *Open Widgets Folder*) and `quote.py` into `~/Library/Application Support/STUDYTERM/standalone/bin/`.
- **Remove:** delete `quote.jsx` from the widgets folder. Your data in `~/Library/Application Support/STUDYTERM/standalone/data/` stays.

## 🎨 Look and position

Out of the box it sits in its default spot in the cyan terminal theme. Install [**WIDGET//CTL**](https://github.com/SlicingReaper/widgetctl) to drag it anywhere on a grid and pick from 16 colour schemes × 8 styles, and to get `⌃⌥⌘W`, which hides all widgets at once.

## 🧩 Part of a collection

This widget is one of fifteen that share the same retro-terminal look, the same theming and the same show/hide hotkey. Each works on its own; together they make a desktop dashboard.

| | Widget | What |
|:-:|:--|:--|
| 💰 | [**WALLET//Ð**](https://github.com/SlicingReaper/points-wallet-widget) | Points wallet: earn for habits, spend on rewards, lock savings, keep a streak |
| 🔥 | [**75//HARD**](https://github.com/SlicingReaper/75-hard-widget) | 75 Hard challenge tracker: 7 daily tasks, day counter, auto-fail on a missed day |
| ⏱️ | [**STUDY//TERM**](https://github.com/SlicingReaper/study-timer-widget) | Study stopwatch that logs what you did, with a stats page and points |
| ✎ | [**NOTE//PAD**](https://github.com/SlicingReaper/notepad-widget) | Checklist notes with deadline countdowns, auto-expiry and a bin |
| “ | [**QUOTE//DAY**](https://github.com/SlicingReaper/quote-of-the-day-widget) ← you are here | A new quote every midnight from a pool of 300, with likes and your own quotes |
| ▦ | [**TETRIS//GRID**](https://github.com/SlicingReaper/tetris-widget) | Tetris on the desktop: hold, ghost piece, levels, best score |
| ◉ | [**PONG//SOLO**](https://github.com/SlicingReaper/pong-widget) | Single-player Pong: keep the ball up, it speeds up every hit |
| ◎ | [**PONG//DUO**](https://github.com/SlicingReaper/pong-duo-widget) | Two-player Pong, 3 widgets wide: W/S vs ↑/↓, first to 7 |
| ⊞ | [**2048//TILE**](https://github.com/SlicingReaper/2048-widget) | 2048 with undo, keyboard or drag, saved between sessions |
| ⌂ | [**OUTPOST//**](https://github.com/SlicingReaper/outpost-colony-widget) | Colony-trading game: claim land, outfit robots, trade against 3 AI rivals |
| ☠ | [**DOOM//TERM**](https://github.com/SlicingReaper/doom-widget) | DOOM shareware Episode 1 in a 2-column widget: WebAssembly engine, savegames kept |
| ◍ | [**GLOBE//GUESS**](https://github.com/SlicingReaper/globe-widget) | Daily mystery country on a spinning globe: every guess glows hotter the closer it is |
| ◍ | [**ATLAS//QUIZ**](https://github.com/SlicingReaper/atlas-quiz-widget) | Sporcle-style map quiz: type a name, the country lights up green. World, continents, US states |
| W | [**WORDLE//**](https://github.com/SlicingReaper/wordle-widget) | The daily five-letter word game: six tries, streaks, guess distribution, unlimited practice |
| 🎛️ | [**WIDGET//CTL**](https://github.com/SlicingReaper/widgetctl) | Menu-bar app that arranges and themes all the widgets, plus a ⌃⌥⌘W show/hide hotkey |

**Install all of them at once:** [`vibecoded` → install-all.command](https://github.com/SlicingReaper/vibecoded) · 🤖 Vibecoded with [Claude](https://claude.ai): I designed, directed and tested it, the AI wrote most of the code.
