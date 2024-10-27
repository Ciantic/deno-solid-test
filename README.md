# SolidStart testing with Deno

Everything you need to build a Solid project, powered by [`solid-start`](https://start.solidjs.com);

## Problem

```shell
deno install

deno run dev # Dev server works






# However
deno run -A build # this does not work, it gives error like:

Task build vinxi build
vinxi v0.4.3

⚙  Building your app...
vinxi v0.4.3
(node:53524) ExperimentalWarning: Importing JSON modules is an experimental feature and might change at any time
(Use `node.EXE --trace-warnings ...` to show where the warning was created)
ReferenceError: Deno is not defined
    at file:///C:/Source/JavaScript/solid-start-test/deno-solid-test/node_modules/.deno/@jsr+std__fs@0.221.0/node_modules/@jsr/std__fs/ensure_symlink.js:7:19
    at ModuleJob.run (node:internal/modules/esm/module_job:222:25)
```

