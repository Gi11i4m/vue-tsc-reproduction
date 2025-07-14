# vue-tsc-reproduction

This is a minimal reproduction of `vue-tsc` version `3` throwing the following error in a Nuxt project.

```
 ERROR(vue-tsc)  File '/Users/gilliamflebus/Projects/iom/vue-tsc-repro/__VLS_fake.d.ts' not found.
 FILE  /Users/gilliamflebus/Projects/iom/vue-tsc-repro/app.vue:8:22

     6 |   </NuxtErrorBoundary>
     7 | </template>
  >  8 | /// <reference path="./__VLS_fake.d.ts" />debugger/* PartiallyEnd: #3632/scriptSetup.vue */
       |                      ^^^^^^^^^^^^^^^^^
     9 | // @ts-ignore
    10 | declare const { defineProps, defineSlots, defineEmits, defineExpose, defineModel, defineOptions, withDefaults, }: typeof import('vue');
    11 | type __VLS_PublicProps = {};

```

To trigger the error, run Nuxt in dev mode with

```
pnpm install
pnpm run dev
```
