# Obsidian Claude Template

Claude Code で Obsidian Vault を活用するためのテンプレート。

## Setup

1. GitHub で空の private リポジトリを作成する（README や .gitignore は追加しない）
2. クローンしてテンプレートをセットアップする

```bash
# 自分のリポジトリをクローン
git clone https://github.com/<your-username>/<your-repo>.git
cd <your-repo>

# テンプレートを upstream として追加
git remote add upstream https://github.com/ymtdir/obsidian-claude-template.git

# テンプレートの内容を取得してマージ
git fetch upstream
git merge upstream/main --allow-unrelated-histories
git push origin main
```

3. Obsidian を開き「Open folder as vault」でクローンしたフォルダを選択する

## Features

### デイリーノートの PDCA ワークフロー

`/daily` コマンドで、1日の記録を PDCA サイクルに沿って整理できます：

| セクション     | PDCA  | 記入者   | 内容                                                                 |
| -------------- | ----- | -------- | -------------------------------------------------------------------- |
| **今日の目標** | Plan  | ユーザー | 朝に今日やるタスクを箇条書きで記入                                   |
| **今日の成果** | Do    | ユーザー | 夜に実際にやったことを自由形式で記入                                 |
| **ふりかえり** | Check | ユーザー | 目標・成果を照らし合わせ、できたこと・できなかったこと・反省点を記入 |
| **まとめ**     | Act   | AI       | ふりかえりを読んで良かった点と改善点をコメント                       |

このワークフローにより、日々の活動から自然に学びを抽出し、継続的な改善につなげることができます。

## Sync

テンプレートの更新を取り込む。

```bash
git fetch upstream
git merge upstream/main
git push origin main
```

下流で `CLAUDE.md` やスキルを編集している場合、マージ時にコンフリクトが発生することがある。その際は手動で解消してからコミットする。
