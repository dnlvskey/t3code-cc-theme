# CC — a T3 Code theme

A theme for [T3 Code](https://github.com/pingdotgg/t3code) (web and desktop) that follows the look of the
Claude Code desktop app: neutral dark greys, an orange accent, serif replies, flat surfaces without glass.

Unofficial. Not affiliated with or endorsed by Anthropic or the T3 Code authors.

## Install

```sh
t3 theme set --id cc cc.t3-theme.json
```

This publishes the file as the theme `cc` on this machine and switches connected clients to it.
To go back, pick any built-in theme in Settings → Appearance, or run `t3 theme set t3-chat`.

Recommended settings: Interface font size 16, Glass opacity 100.

## What it changes

Colors are set through T3 Code's color roles, for both dark and light appearance. Both palettes were
measured from the Claude Code desktop app. Dark: canvas `#191919`, sidebar `#1f1f1f`, selected row
`#404040`, composer `#303030`, accent `#d97757`. Light: canvas `#ffffff`, sidebar `#fafafa`, selected
row `#e1e1e1`, borders `#e5e5e5`, text `#191919`.

The CSS is 19 short rules built on T3 Code's `data-*` attributes and its documented selectors:

- **No glass.** Backdrop filters are off, glass surfaces are opaque, and the sidebar has no grain texture.
  The Glass opacity setting has no effect with this theme.
- **Chat text.** Replies and your messages are 15px; replies use Georgia with a 1.5 line height.
  In replies, headings are body-sized and bold, lists have a wider indent, tables use the body size,
  and inline code has a flat grey background.
- **Details panel.** Flat, without the card background and border.
- **Project icons.** A folder outline in the icon color instead of the colored monogram tile.
- **Sharp text on Windows.** The chat and sidebar scrollers get an opaque background so that their text
  is rendered with ClearType.
- **Composer.** A `#404040` outline in dark mode, `#ddd` in light, and a rounded-square send button.
- **No blue.** The working status, info messages and the quote, file, image, video and mention chips
  use the orange accent instead of T3 Code's blues. "Awaiting Input" is yellow, like "Approval".
- **Calm chips.** Skill, model, thread, environment, terminal, element, review and pull-request chips
  are grey. Pull-request states and document types keep their own colors.
- **Quotes in sent messages.** No highlight box behind the quoted text.

The interface font, popups, scrollbars and layout are left as T3 Code ships them.

## Limits

- Themes do not apply to the T3 Code mobile app.
- A theme cannot load font files, so the Anthropic typefaces are not used.
- Checked on T3 Code Nightly for Windows only.

## License

MIT
