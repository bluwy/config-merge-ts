# config-merge-ts

Test merging config interfaces and intellisense.

## Explanation

This repo has three fake libraries under `node_modules`, which is intentionally committed to git. Do not run `npm i`.

There are three libraries, `@sveltejs/config`, `foo`, and `bar`. `foo` and `bar` are libraries that want to extend the Svelte config definition from `@sveltejs/config`, so that they are typed in `svelte.config.js`. See the type definitions:

- [foo/index.d.ts](./node_modules/foo/index.d.ts)
- [bar/index.d.ts](./node_modules/bar/index.d.ts)
- [@sveltejs/config/index.d.ts](./node_modules/@sveltejs/config/index.d.ts)

To test intellisense, go to [svelte.config.js](./svelte.config.js) and try typing props for `foo` and `bar`.

## Reference

- Docs: https://www.typescriptlang.org/docs/handbook/declaration-merging.html
- Idea: https://github.com/sveltejs/kit/issues/3569#issuecomment-1024999620
