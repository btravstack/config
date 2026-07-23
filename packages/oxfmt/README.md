# @btravstack/oxfmt

Shared [oxfmt](https://oxc.rs) settings for btravstack packages.

> **oxfmt has no `extends` mechanism.** Unlike the other packages here, this one
> is a **copy-template**, not something you inherit at runtime. It exists so the
> canonical settings live in one versioned place; copy them into your repo.

```sh
pnpm add -D @btravstack/oxfmt oxfmt
```

Copy `node_modules/@btravstack/oxfmt/base.json` into your `.oxfmtrc.json` and add
repo-specific `ignorePatterns`:

```jsonc
// .oxfmtrc.json
{
  "$schema": "./node_modules/oxfmt/configuration_schema.json",
  "ignorePatterns": ["pnpm-lock.yaml"],
  "sortImports": true,
}
```

MIT © Benoit Travers
