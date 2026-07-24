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
`noImplicitOverride`, `noImplicitReturns`, `verbatimModuleSyntax`,
`moduleDetection: "force"`, and friends, on `NodeNext` / `ES2022`. Override
anything in your own `compilerOptions`.

It does **not** set `types` — TypeScript auto-includes every reachable
`@types/*` package (Node included). This avoids forcing each consuming package to
declare a direct `@types/node` just to satisfy a `types: ["node"]` list.

MIT © Benoit Travers
