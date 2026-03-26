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

## Sync

テンプレートの更新を取り込む。

```bash
git fetch upstream
git merge upstream/main
git push origin main
```

下流で `CLAUDE.md` やスキルを編集している場合、マージ時にコンフリクトが発生することがある。その際は手動で解消してからコミットする。
