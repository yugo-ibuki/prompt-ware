# Cursor

## 重要なこと

- rulesは英語で書くこと(AIが理解しやすくなる)
- rulesは複数に分けて書く

## グローバルGitIgnoreの設定

全プロジェクトで `rules` ディレクトリを除外するための設定:

1. グローバルなgitignoreファイルを作成:
```bash
# まずファイルを作成
touch ~/.gitignore_global

# グローバル設定を行う
git config --global core.excludesfile ~/.gitignore_global
```

2. ~/.gitignore_global に以下を追加:
```bash
# 以下の内容をファイルに追記
echo '# Cursor用rulesディレクトリ
**/rules/' >> ~/.gitignore_global
```

または、エディタで直接編集する場合は以下の内容を追加:
```gitignore
# Cursor用rulesディレクトリ
**/rules/
```

この設定により、プロジェクト内のどの階層にある `rules` ディレクトリも自動的にGit管理から除外されます。

設定後の確認方法:
```bash
# 設定が正しく行われたか確認
git config --global --get core.excludesfile

# gitignoreの内容を確認
cat ~/.gitignore_global
```

## cursorrulesを拡張するためのメモ

cursorのruleを書くための資料
https://zenn.dev/nagisora/articles/ea823063a0e9c3#pontus-abrahamsson

mizchiさんのailab
https://github.com/mizchi/ailab

project rulesについて
https://zenn.dev/globis/articles/cursor-project-rules
