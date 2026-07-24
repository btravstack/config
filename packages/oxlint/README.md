# @btravstack/oxlint

Shared [oxlint](https://oxc.rs/docs/guide/usage/linter) config for btravstack
packages.

```sh
pnpm add -D @btravstack/oxlint oxlint
```

oxlint resolves `extends` by **file path** (relative to the config file), so
point at the file inside `node_modules`:

```jsonc
// .oxlintrc.json
{
  "$schema": "./node_modules/oxlint/configuration_schema.json",
  "extends": ["./node_modules/@btravstack/oxlint/base.json"],
  "ignorePatterns": ["dist/**"],
}
```

`base.json` enables:

- `@typescript-eslint/no-explicit-any` — `error`
- `@typescript-eslint/consistent-type-imports` — `error` (type-only imports must use
  a `type` specifier; autofixable with `oxlint --fix`, inline style)
- `typescript/consistent-type-definitions` — `["error", "type"]` (no `interface`)

Add your own rules and `ignorePatterns` in the consuming config; later entries
override earlier ones.

MIT © Benoit Travers
