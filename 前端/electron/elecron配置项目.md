### 0.1 ts中引入path模块出错

Cannot find module 'path' or its corresponding type declarations.
##### 第一步

```bash
npm install -D @types/node
```

```bash
cnpm install -D @types/node
```
##### 第二步
在tsconfig.json中添加

```json
"compilerOptions": {
	"types": [
      "node"
    ]
}
```