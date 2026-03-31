# @fandhe-ai/shared-config-commitlint

Commitlint の共有設定。Conventional Commits + pnpm workspace スコープを提供。

## エクスポート

| パス | 説明 |
|------|------|
| `@fandhe-ai/shared-config-commitlint/base` | `@commitlint/config-conventional` + `@commitlint/config-pnpm-scopes` を extends |

## 使用方法

`commitlint.config.ts` で `extends` に指定する:

```ts
export default {
  extends: ["@fandhe-ai/shared-config-commitlint/base"],
  rules: {
    "scope-enum": [2, "always", ["global", "web", "storybook"]],
  },
};
```

## 開発

### セットアップ

```bash
pnpm install
```

### コミット規約

[Conventional Commits](https://www.conventionalcommits.org/ja/) を採用。
[commitlint](https://commitlint.js.org/) + [lefthook](https://github.com/evilmartians/lefthook) により自動検証。

```
<type>: <description>

# 例
feat: 新しいルールを追加
fix: 設定の不具合を修正
chore: 依存関係を更新
```

## ライセンス

Copyright © Fandhe Inc.
