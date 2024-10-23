# SolidStart testing with Deno

Everything you need to build a Solid project, powered by [`solid-start`](https://start.solidjs.com);

## Problem

```
deno install

deno run dev

```

Navigate to http://localhost:3000, you will get import error such as:

```
11.51.12 [vite] Error when evaluating SSR module C:/Source/JavaScript/solid-start-test/deno-solid-test/src/routes/index.tsx?pick=default&pick=$css: failed to import "jsr:@db/sqlite@0.12"
|- Error: Cannot find module 'jsr:@db/sqlite@0.12' imported from 'C:/Source/JavaScript/solid-start-test/deno-solid-test/src/db/db.ts'
    at nodeImport (C:\Source\JavaScript\solid-start-test\deno-solid-test\node_modules\.deno\vite@5.4.9\node_modules\vite\dist\node\chunks\dep-Cyk9bIUq.js:53036:19)        
    at ssrImport (C:\Source\JavaScript\solid-start-test\deno-solid-test\node_modules\.deno\vite@5.4.9\node_modules\vite\dist\node\chunks\dep-Cyk9bIUq.js:52903:22)
    at undefined
    at async instantiateModule (C:\Source\JavaScript\solid-start-test\deno-solid-test\node_modules\.deno\vite@5.4.9\node_modules\vite\dist\node\chunks\dep-Cyk9bIUq.js:52961:5)
```

This most likely because Vinxi runs `node.exe` behind the scenes instead of `deno.exe`.