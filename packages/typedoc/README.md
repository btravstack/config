# @btravstack/typedoc

Shared TypeDoc (markdown) configuration for btravstack packages.

```sh
pnpm add -D @btravstack/typedoc typedoc typedoc-plugin-markdown
```

```jsonc
// typedoc.json
{
  "extends": "@btravstack/typedoc/base.json",
  "entryPoints": ["src/index.ts"],
  "out": "docs",
}
```

`base.json` configures the markdown plugin, table-based formatting, and the
exclusions used across btravstack docs. `typedoc` and `typedoc-plugin-markdown`
are peer dependencies — install them alongside.

MIT © Benoit Travers
