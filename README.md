# Mayukai for Zed

A vibecoded port of Mayukai Dark from GulajavaMinistudio's
[Mayukai Theme](https://github.com/GulajavaMinistudio/Mayukai-Theme) for
VS Code, version 3.3.0.

> [!WARNING]
> I tuned this specifically for C++ first and C second. A Zed theme gives each
> tree-sitter capture one style in every language, and it cannot set a style
> per language, which is different from VS Code.
>
> This means that, where Mayukai colors the same capture differently in two
> languages, the C++ color wins, so other languages can differ from expectations.
>
> Keep this is mind if you plan to use it for other languages.

## Install

The extension is not in the Zed registry yet. Clone this repository, run
`zed: install dev extension` from the command palette, and pick the clone.
Then choose "Mayukai Dark" in the theme selector.

To use the theme file alone, copy `themes/mayukai.json` into
`~/.config/zed/themes/`.

## License

MIT, the same license as the original theme.
