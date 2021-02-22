TypeScript Node tsconfig-paths Demo
============================

在tsconfig.json中定义的`paths`仅供typescript类型检查使用。当它被编译成js时，并不会被替换，所以node无法直接执行。

node配合`tsconfig-paths`使用，可以动态替换。

这种做法不太好的地方必须在ts文件旁边生成js文件，实际项目中不可能这么做。一个更好的办法是使用ts-node避免js生成。
见另一个demo


```
npm install
npm run demo
```

注意：
如果tsconfig.json中使用`outDir`把js代码产生到了另一个目录，比如`dist`，则无法正常工作。
因为它从tsconfig.json中读取的paths定义指向的还是`src`目录，会报以下错误。

```
Cannot find module '#src/utils/util1'
```

此时需要通过代码方式配置tsconfig-paths，手动进行替换。见另一个demo
