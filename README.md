TypeScript Node tsconfig-paths Demo
============================

在tsconfig.json中定义的`paths`仅供typescript类型检查使用。当它被编译成js时，并不会被替换，所以node无法直接执行。

node配合`tsconfig-paths`使用，可以动态替换。

```
npm install
npm run demo
```

Problem:

提示： Cannot find module '#src/utils/util1'

不知道问题在哪儿
