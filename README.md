reproduce repo of vue-tsc issue

1. run `pnpm install`
2. check `apps/vue2-project/src/Foo.vue` line 11, ts will report an error(ts(2339))
3. check `apps/vue2-project/src/main.ts` line 14, there is no error(If takeover is enabled, this file reports error too).

I lift `vite` from `vue2-project` and move it to the root of monorepo, `vue-tsc` seems behave inconsistently with `tsc`, it does not recognize `vite/client` defined in `packages/tsconfig/vue-app.json`.
