# MS-DOS for Multica

The 16-colour DOS look as a [Multica](https://multica.ai) theme. Light mode is DOS Shell: grey frame, white panes and a blue selection bar. Dark mode is a text-mode screen, with inverse-video selection, square corners, hard drop shadows and the IBM VGA 8×16 font throughout.

Install it from **Settings → Appearance → Manage** in Multica, or download `theme.zip` from the latest release and import it.

## Options

- **Screen (dark mode)**: `C:\>` prompt (default, grey on black), MS-DOS Editor (white on blue), amber phosphor or green phosphor.
- **Font**: IBM VGA 8×16 (default) or a modern monospace (Cascadia Mono, Consolas or Menlo, whichever is installed). Choose the modern one if the bitmap font is hard to read at your display scale.
- **Blinking cursor after headings**: on by default. It stays still when your system asks for reduced motion.

The VGA font has a single weight, so bold text is drawn in the brighter colour of each screen instead of being thickened.

## Develop

From a checkout of [multica-ai/multica](https://github.com/multica-ai/multica):

```bash
pnpm theme:check ../multica-microsoft-dos     # validator and contrast checks
pnpm theme:preview ../multica-microsoft-dos   # light.png and dark.png
```

The checks run with each option at its default. To check another screen, set its `default` in `manifest.json` for the run.

To release, bump `version` in `manifest.json`, tag the commit with the same version (`v1.1.0`), and push the tag. The release workflow attaches `theme.zip`; the [theme store](https://github.com/multica-ai/multica-themes) picks it up within the hour once it passes the checks.

## License

The theme is MIT. The font in `fonts/vga-8x16.woff` is "WebPlus IBM VGA 8x16" from [The Ultimate Oldschool PC Font Pack](https://int10h.org/oldschool-pc-fonts/) by VileR, licensed under [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/) (`fonts/LICENSE-FONT.txt`).

MS-DOS is a trademark of Microsoft. This theme is not affiliated with or endorsed by Microsoft.
