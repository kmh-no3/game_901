# GitHubへのアップロード手順

## 1. GitHubリポジトリの作成

1. GitHubにログインして、https://github.com/new にアクセス
2. リポジトリ名を入力（例: `game_901`）
3. 「Public」を選択（GitHub Pagesは無料で利用可能）
4. 「Initialize this repository with a README」は**チェックしない**
5. 「Create repository」をクリック

## 2. ローカルでGitリポジトリを初期化

ターミナルで以下のコマンドを実行してください：

```bash
cd "/Users/hosodakenji/Library/CloudStorage/GoogleDrive-lmbd.cs2nc.manga@gmail.com/マイドライブ/ゲーム開発/参考/901/game_901"
git init
git add .
git commit -m "Initial commit: Game template"
```

## 3. GitHubリポジトリと接続

GitHubで作成したリポジトリのURLを取得して、以下のコマンドを実行：

```bash
git remote add origin https://github.com/あなたのユーザー名/game_901.git
git branch -M main
git push -u origin main
```

## 4. GitHub Pagesで公開する

1. GitHubリポジトリのページで「Settings」タブをクリック
2. 左側のメニューから「Pages」を選択
3. 「Source」セクションで：
   - 「Branch」を選択
   - 「main」ブランチを選択
   - 「/ (root)」を選択
4. 「Save」をクリック

**注意**: `index.html`はルートディレクトリに配置されているため、ルートを選択してください。

## 5. 公開URLの確認

数分後、以下のURLでゲームにアクセスできます：
- `https://あなたのユーザー名.github.io/game_901/`

## 注意事項

- GitHub Pagesは静的サイトのみサポート（サーバーサイドの処理は不可）
- このゲームは完全にクライアントサイドで動作するため、問題なく動作します
- 画像ファイル（.png）も正しく読み込まれます

