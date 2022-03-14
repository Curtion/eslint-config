个人使用的eslint配置。


使用 `https://github.com/antfu/eslint-config`

# 依赖

 - @antfu/eslint-config
 - eslint-plugin-vue
 - typescript

# 配置

`.eslintrc`：

```javascript
{
  "extends": "@antfu",
  "rules": {
    "curly": [ //强制if等语句添加大括号
      "error",
      "all"
    ],
    "brace-style": [ //强制大括号不换行
      "error",
      "1tbs"
    ],
    "@typescript-eslint/brace-style": ["error", "1tbs"]
  },
  "env": {
    "vue/setup-compiler-macros": true
  }
}
```

`.eslintignore`:

```
node_modules/*
```