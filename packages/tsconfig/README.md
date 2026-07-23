# @btravstack/tsconfig

Shared strict TypeScript configuration for btravstack packages.

```sh
pnpm add -D @btravstack/tsconfig
```

```jsonc
// tsconfig.json
{
  "extends": "@btravstack/tsconfig/base.json",
  "compilerOptions": { "outDir": "./dist", "rootDir": "./src" },
  "include": ["src/**/*"],
}
```

`base.json` enables `strict`, `exactOptionalPropertyTypes`,
`noUncheckedIndexedAccess`, `noPropertyAccessFromIndexSignature`,
`noImplicitOverride`, `noImplicitReturns`, and friends, on `NodeNext` /
`ES2022`. Override anything in your own `compilerOptions`.

MIT © Benoit Travers
