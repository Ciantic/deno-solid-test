# SolidStart testing with Deno

Everything you need to build a Solid project, powered by [`solid-start`](https://start.solidjs.com);

## Problem

```shell
deno install

deno run dev # Dev server works






# However this does not work, it gives error like:
$ deno run -A build # 

deno run -A --node-modules-dir npm:vinxi build
vinxi v0.4.3


⚙  Building your app...
vinxi v0.4.3
(node:33840) ExperimentalWarning: Importing JSON modules is an experimental feature and might change at any time
(Use `node.EXE --trace-warnings ...` to show where the warning was created)
ReferenceError: Deno is not defined
    at file:///C:/Source/JavaScript/solid-start-test/deno-solid-test/node_modules/.deno/@jsr+std__fs@0.221.0/node_modules/@jsr/std__fs/ensure_symlink.js:7:19
    at ModuleJob.run (node:internal/modules/esm/module_job:222:25)
    at async ModuleLoader.import (node:internal/modules/esm/loader:316:24)
    at async loadFile (file:///C:/Source/JavaScript/solid-start-test/deno-solid-test/node_modules/.deno/vinxi@0.4.3/node_modules/vinxi/lib/load-app.js:83:25)
    at async loadApp (file:///C:/Source/JavaScript/solid-start-test/deno-solid-test/node_modules/.deno/vinxi@0.4.3/node_modules/vinxi/lib/load-app.js:137:19)
    at async Object.run (file:///C:/Source/JavaScript/solid-start-test/deno-solid-test/node_modules/.deno/vinxi@0.4.3/node_modules/vinxi/bin/cli.mjs:229:17)
    at async runCommand (file:///C:/Source/JavaScript/solid-start-test/deno-solid-test/node_modules/.deno/citty@0.1.6/node_modules/citty/dist/index.mjs:316:16)
    at async runCommand (file:///C:/Source/JavaScript/solid-start-test/deno-solid-test/node_modules/.deno/citty@0.1.6/node_modules/citty/dist/index.mjs:307:11)
    at async runMain (file:///C:/Source/JavaScript/solid-start-test/deno-solid-test/node_modules/.deno/citty@0.1.6/node_modules/citty/dist/index.mjs:445:7)

 ERROR  Couldn't load app                                                                                                                                              22.43.35  

  at Object.run (/C:/Source/JavaScript/solid-start-test/deno-solid-test/node_modules/.deno/vinxi@0.4.3/node_modules/vinxi/bin/cli.mjs:231:12)
  at async runCommand (/C:/Source/JavaScript/solid-start-test/deno-solid-test/node_modules/.deno/citty@0.1.6/node_modules/citty/dist/index.mjs:316:16)
  at async runCommand (/C:/Source/JavaScript/solid-start-test/deno-solid-test/node_modules/.deno/citty@0.1.6/node_modules/citty/dist/index.mjs:307:11)
  at async runMain (/C:/Source/JavaScript/solid-start-test/deno-solid-test/node_modules/.deno/citty@0.1.6/node_modules/citty/dist/index.mjs:445:7)



 ERROR  Couldn't load app                                                                                                                                              22.43.35  


 ERROR  Exited with code: 1                                                                                                                                            22.43.35  

  at CommandChild.pipedStdoutBuffer (/C:/Source/JavaScript/solid-start-test/deno-solid-test/node_modules/.deno/dax-sh@0.39.2/node_modules/dax-sh/esm/mod.js:9392:19)
  at eventLoopTick (ext:core/01_core.js:175:7)



 ERROR  Exited with code: 1                                   
```

Notably it's trying to run node.EXE given from error message.