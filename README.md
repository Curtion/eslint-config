个人使用的eslint配置。


使用 `https://github.com/antfu/eslint-config`

# 依赖

 - @antfu/eslint-config
 - eslint
 - @eslint/eslintrc (可选)

# 配置

`eslint.config.js`：

```javascript
import antfu from '@antfu/eslint-config'
import FlatCompat from '@eslint/eslintrc'

const compat = new FlatCompat()

export default antfu(
  {
    typescript: true,
    vue: true,
    ignores: [],
  },
  ...compat.config({
    root: true,
    parserOptions: {},
    extends: [],
    plugins: [],
    env: {},
    overrides: [],
  }),
  {
    rules: {
      'no-console': 'error', // 允许使用console
      'curly': 'error', // if等语句添加大括号
      'brace-style': '1tbs', // 大括号不换行
    },
  },
)
```


`.vscode/settings.json`：

```json
{
  "eslint.experimental.useFlatConfig": true
}
```