
TypeScript compiler can handle this code, but `dts2hx` cannot.

```
$ npm install typescript
$ npx tsc
$ node index.js
Hello
```


How to reproduce the problem:
```
$ npm install dts2hx --save-dev
$ npx dts2hx @dts2hx-issue/foo
> Converting module @dts2hx-issue/foo
> Error: Failed to get sourceFile "path/to/research-misc/dts2hx-issue/node_modules/@dts2hx-issue/hoge/index.d.ts"
```

error message says that `dts2hx` cannot read `@dts2hx-issue/hoge/index.d.ts` file, but it exists.


