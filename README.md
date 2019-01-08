# Goal:

no-hoisting of submodule dependencies.

Therefore a should not contain the @types of b, c and d in a/node_modules/@types.

Suggestion in [yarn ticket](https://github.com/yarnpkg/yarn/issues/5620) does not work.

# Package dependencies:

```bash
├── a
│   ├── node_modules
│   │   ├── b -> ../../b
│   └── package.json
├── b
│   ├── node_modules
│   │   ├── c -> ../../c
│   │   ├── d -> ../../d
│   └── package.json
├── c
│   ├── node_modules
│   │   ├── d -> ../../d
│   └── package.json
├── d
│   └── package.json
```
