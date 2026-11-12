# Mayukai for Zed

A port of Mayukai Dark from GulajavaMinistudio's
[Mayukai Theme](https://github.com/GulajavaMinistudio/Mayukai-Theme) for
VS Code, version 3.3.0.

## Install

The extension is not in the Zed registry yet. Clone this repository, run
`zed: install dev extension` from the command palette, and pick the clone.
Then choose "Mayukai Dark" in the theme selector.

To use the theme file alone, copy `themes/mayukai.json` into
`~/.config/zed/themes/`.

## Differences from VS Code

> [!WARNING]
> This port is tuned for C++ first and C second. A Zed theme gives each
> tree-sitter capture one style in every language, and it cannot set a style
> per language. Where Mayukai colors the same capture differently in two
> languages, the C++ color wins, so other languages can differ from VS Code.
> YAML keys are `#fc4085` in VS Code and plain here, because Zed captures them
> as `property`, the capture it also uses for C++ fields.

With `"semantic_tokens": "off"`, C and C++ differ from VS Code in these places:

- Keywords are upright. VS Code italicizes `class`, `struct`, `enum`, `union`,
  `namespace`, `template`, `typename` and the access specifiers, and leaves
  `static`, `const`, `virtual` and `constexpr` upright. Zed captures all of
  them as `keyword`.
- `class Name` looks like `struct Name`, with an orange keyword and a
  `#ff8f40` name. VS Code colors both words of the class form `#f07178`.
- In C, primitive types use the type-name color `#ff8f40`. VS Code shows them
  in italic `#95e6cb`. C++ primitives are italic `#ffa759` in both editors.
- Parameters are plain. Zed's C and C++ queries do not capture them.
- `sizeof`, `new` and `delete` are keyword orange, and `.` and `->` are
  operator pink. VS Code has them as operators and dim separators.
- C++ identifiers in capitals use the `nullptr` color `#f29668`. Zed's C++
  query captures both as `constant.builtin`.

In other languages the larger differences are control-flow keywords in Python
and TypeScript (`#f07178` in VS Code, orange here), booleans in TypeScript,
JSON, Go and YAML (`#d4bfff` in VS Code, `#f29668` here), and YAML keys
(`#fc4085` in VS Code, plain here).

## License

MIT, the same license as the original theme.
