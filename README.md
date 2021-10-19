# Rematch Bug `object is not extensible`

[![CodeSandbox](https://codesandbox.io/static/img/play-codesandbox.svg)](https://codesandbox.io/s/amazing-joliot-2qcez)

This is a reproduce of the following `object is not extensible` bug:

```
TypeError
Cannot add property loading, object is not extensible
    at onModel (https://2qcez.csb.app/node_modules/
rematch/updated/dist/updated.esm.js:55:27
    at eval (https://2qcez.csb.app/node_modules/
rematch/core/dist/core.esm.js:273:5
    at eval (https://2qcez.csb.app/node_modules/
rematch/core/dist/core.esm.js:207:11
    at Object.forEachPlugin (https://2qcez.csb.app/node_modules/
rematch/core/dist/core.esm.js:205:22
    at prepareModel (https://2qcez.csb.app/node_modules/
rematch/core/dist/core.esm.js:272:7
    at eval (https://2qcez.csb.app/node_modules/
rematch/core/dist/core.esm.js:248:12
    at createRematchStore (https://2qcez.csb.app/node_modules/
rematch/core/dist/core.esm.js:247:14
    at init (https://2qcez.csb.app/node_modules/
rematch/core/dist/core.esm.js:336:10
$csb$eval
/src/Demo/store.ts:10:49
   7 |
   8 | type FullModel = ExtraModelsFromLoading<IRootModel> &
   9 |   ExtraModelsFromUpdated<IRootModel>;
> 10 | export const store = init<IRootModel, FullModel>({
     |                                                 ^
  11 |   models,
  12 |   plugins: [updated(), loading(), immerPlugin(), selectPlugin()]
  13 | });
View compiled
▶ 4 stack frames were collapsed.
```
