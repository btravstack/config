# @btravstack/commitlint

Shared [commitlint](https://commitlint.js.org) preset for btravstack packages —
conventional commits.

```sh
pnpm add -D @btravstack/commitlint @commitlint/cli
```

```js
// commitlint.config.js
export default { extends: ["@btravstack/commitlint"] };
```

Wraps `@commitlint/config-conventional` (bundled as a dependency).
`@commitlint/cli` is a peer — install it alongside, and wire it into your
commit-msg hook (see [`@btravstack/lefthook`](../lefthook)).

MIT © Benoit Travers
