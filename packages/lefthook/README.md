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
```

Provides:

- **pre-commit** — `oxfmt` (with `stage_fixed`) and `oxlint` on staged files
- **commit-msg** — `commitlint --edit`

It assumes `oxfmt`, `oxlint`, and `commitlint` are available in the consumer
(pair with [`@btravstack/oxfmt`](../oxfmt), [`@btravstack/oxlint`](../oxlint),
[`@btravstack/commitlint`](../commitlint)). Extend or override any command in
your own `lefthook.yml`; run `pnpm exec lefthook install` once to register the
hooks.

MIT © Benoit Travers
