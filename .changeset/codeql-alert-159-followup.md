---
"@pnpm/pkg-manifest.utils": patch
"pnpm": patch
---

`convertEnginesRuntimeToDependencies`: switch the runtime-dependency write to `Object.defineProperty` so the CodeQL `js/prototype-polluting-assignment` rule treats the assignment as safe regardless of the property name (follow-up to [#11609](https://github.com/pnpm/pnpm/pull/11609)).
