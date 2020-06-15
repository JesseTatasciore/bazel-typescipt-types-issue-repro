Running bazel version 3.2.0

Make sure to `bazel clean` between runs

`bazel build //...` (will go green)

`bazel build --strategy=TypeScriptCompile=worker //...` (will go green)

`bazel build --strategy=TypeScriptCompile=local //...` (will fail)

```
ERROR: .../bazel-typescipt-types-issue-repro/BUILD:14:11: Compiling TypeScript (devmode) //:semver failed (Exit 1)
semver.ts:1:25 - error TS2307: [strictDeps] transitive dependency on external/npm/node_modules/@types/semver/index.d.ts not allowed. Please add the BUILD target to your rule's deps.

1 import * as semver from 'semver';
```
