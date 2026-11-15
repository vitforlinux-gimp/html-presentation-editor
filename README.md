# Presentation Editor

A self-contained HTML presentation editor. **One file. No build. No server.** Open it in your browser, click any text, type. Cmd+S writes back to the same file. Send the file to anyone — they can read it, or edit it the same way you did.

![Editor in light theme](screenshots/hero-light.png)

**[Try it live →](https://vitforlinux-gimp.github.io/editor.html)** · **[Download v1.0.3](https://github.com/vitforlinux-gimp/html-presentation-editor/releases/latest)**


## Why

You wanted a beautiful slide. They gave you a PDF: nice, but you can't edit it.
Or HTML: you can edit it, but only in the source.

This is an attempt to have both a slide and a simple editable HTML website.

There are popular products, but they block and require an account... and sometimes annual payments.

This is a single HTML file that edits itself. The whole product is the file. The file is the whole product.

## Features

- **One file, zero dependencies.** ~52 KB of vanilla HTML/CSS/JS. No npm, no build, no server.
- **9 block types.** Hero, heading, text, two-column, image+text,Image-BIG, list, quote, code.
- **In-page editing.** Click any text. Hover any block to move, duplicate, or delete it.
- **Two views.** Document mode (scroll) or Slides mode (full-screen, arrow-key nav).
- **3 themes × 4 accent palettes.** Light, dark, sepia × default-blue, mono, warm, green.
- **Image swap.** Click any image, pick a local file — embedded as base64. File stays self-contained.
- **PDF export.** `Cmd+P` opens the native print dialog with proper page breaks.
- **Auto-save** to `localStorage` as a safety net. "Restore unsaved" banner if the browser crashed.

## Quick start

1. [Download `editor.html`](https://github.com/vitforlinux-gimp/html-presentation-editor/blob/main/editor.html) (or [grab the source](editor.html), or [try it live](https://vitforlinux-gimp.github.io/editor.html) without downloading).
2. Open it in your browser.
3. Click any text and type. `Cmd+S` to save.

That's it. No setup.

## How saving works

| Browser | Behavior |
|---------|----------|
| Chrome, Edge, Brave, Opera | First `Cmd+S` opens a save dialog. Pick the same file to overwrite it. After that, `Cmd+S` writes silently in place. ([File System Access API](https://developer.mozilla.org/en-US/docs/Web/API/File_System_Access_API)) |
| Safari, Firefox | `Cmd+S` downloads the updated file. Replace the original manually. |

The saved file is a fully working editor — open it again to keep editing. Toolbar, controls, and inserted UI never touch the disk; they're injected by JS on load and stripped on save.

## Keyboard shortcuts

| Key | Action |
|-----|--------|
| `E` | Toggle edit / preview |
| `S` | Toggle doc / slides mode |
| `Cmd+S` | Save |
| `Cmd+P` | Print / export PDF |
| `← →`, Space | Navigate slides (in slides mode) |
| `?` | Show all shortcuts |
| `Esc` | Close dialogs / unfocus |

## Screenshots

| Light | Dark | Sepia |
|-------|------|-------|
| ![Light](screenshots/hero-light.png) | ![Dark](screenshots/hero-dark.png) | ![Sepia](screenshots/hero-sepia.png) |

| Slides mode | Insert block picker | Hover controls |
|-------------|---------------------|----------------|
| ![Slides](screenshots/slides-mode.png) | ![Picker](screenshots/insert-picker.png) | ![Controls](screenshots/block-controls.png) |

## Browser support

- **Full features:** Chromium-based browsers (Chrome 86+, Edge, Brave, Opera, Arc).
- **Edit + download save:** Safari 16+, Firefox 100+.
- **Tested on:** Chromium 1217 via Playwright (zero console errors).

## Project layout

```
editor.html          ← the entire product
screenshots/         ← README assets
LICENSE              ← MIT
README.md            ← this file
```

## Contributing

Issues and PRs welcome. Keep it simple — the constraint is "one file, no dependencies." If a feature needs a build step or third-party library, it probably belongs in a fork, not here.

## License

[MIT](LICENSE) — do whatever you want.

# Things done and dreams

## Done
- Fixed up and down slide
- Fixed Image+Text
- Added Lazy loading for images
- Fixed Two column slide
- Added Image BIG slide
- Update README after fork
- Fixed 98 JavaScript errors THANKS! [HTML Validator](https://addons.mozilla.org/en-US/firefox/addon/html-validator)
- Add/remove URL in paragraph
- Bold text in paragraph
- Italic text in paragraph
- Inline code in paragraph
- Align left
- Align center
- Align right
- Three svg buttons 
- Remove formatting
- Fixed other new JavaScript AI errors THANKS! [HTML Validator](https://addons.mozilla.org/en-US/firefox/addon/html-validator)
- Translate in english italian alerts and labels (AI errors!)


## Dreams
- ~~Add/remove/edit URL in paragraph~~
- ~~Bold text in paragraph~~
- ~~Italic text in paragraph~~
- ~~Inline code in paragraph~~
- Background color for single slide
- Background image for all slides
- Background image for single slide
- Disable editing/slides only javascript variable
- Side navigation bar
- Search in slides
- Opacity in themes

## Credits

- Idea by [@gleb_pro_ai (post 558)](https://t.me/gleb_pro_ai/558)
- Built with [Claude Code](https://claude.com/claude-code) by Ilya Chernetskiy
- Fix/Update with [TGPT](https://github.com/aandrew-me/tgpt) , [HTML Validator](https://addons.mozilla.org/en-US/firefox/addon/html-validator), Google Gemini, hand, eyes, brain by Vitforlinux
