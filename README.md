个人使用的eslint配置。


使用 `https://github.com/antfu/eslint-config`

# 依赖

`pnpm install eslint @antfu/eslint-config`

# 配置

`eslint.config.js`：

```javascript
import antfu from '@antfu/eslint-config'

export default antfu(
  {
    typescript: true,
    vue: true,
    ignores: [],
  },
  {
    rules: {
      'no-console': ['off'], // 允许使用console
      'style/brace-style': ['error', '1tbs'], // 大括号风格
      'curly': ['error', 'all'], // 控制语句后必须有{}
    },
  },
)
```

