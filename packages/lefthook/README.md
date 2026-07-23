# @btravstack/lefthook

Shared [lefthook](https://lefthook.dev) git-hooks preset for btravstack
packages.

```sh
pnpm add -D @btravstack/lefthook lefthook
```

```yaml
# lefthook.yml
extends:
  - node_modules/@btravstack/lefthook/lefthook.yml

# Excludes are repo-specific — declare them locally (they merge into the base
# commands). At minimum exclude the lockfile from formatting:
pre-commit:
  commands:
    format:
      exclude:
        - "pnpm-lock.yaml"
        # - "docs/api/*"   # + any generated dirs this repo produces
```

Provides:

- **pre-commit** — `oxfmt` (with `stage_fixed`) and `oxlint` on staged files
- **commit-msg** — `commitlint --edit`

**On excludes:** the base sets **no** `exclude` on its commands, by design.
lefthook's `extends` merge lets the extended (base) file _override_ the local one
for keys it defines — so if the base set `format.exclude`, a consumer couldn't
layer its own on top. Because the base omits it, each repo declares its full
`exclude` list locally and it merges in. Every consumer should at least exclude
`pnpm-lock.yaml` from formatting.

It assumes `oxfmt`, `oxlint`, and `commitlint` are available in the consumer
(pair with [`@btravstack/oxfmt`](../oxfmt), [`@btravstack/oxlint`](../oxlint),
[`@btravstack/commitlint`](../commitlint)). Run `pnpm exec lefthook install`
once to register the hooks.

MIT © Benoit Travers
