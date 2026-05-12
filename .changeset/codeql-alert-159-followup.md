---
"@pnpm/pkg-manifest.utils": patch
"pnpm": patch
---

`convertEnginesRuntimeToDependencies`: switch the runtime-dependency write to `Object.defineProperty` so CodeQL's `js/prototype-polluting-assignment` analyser recognises the assignment as safe regardless of the property name (follow-up to [#11609](https://github.com/pnpm/pnpm/pull/11609)).
