# GitHub Pages 404エラー トラブルシューティング

## 現在の状況

404エラーが表示される場合、以下の点を確認してください。

## 確認事項

### 1. GitHub Pagesが有効になっているか確認

1. GitHubリポジトリにアクセス: https://github.com/kmh-no3/game_901
2. 「Settings」タブをクリック
3. 左側のメニューから「Pages」を選択
4. 「Source」セクションを確認：
   - 「Branch」が選択されているか
   - 「main」ブランチが選択されているか
   - 「/ (root)」が選択されているか
5. 「Save」をクリック（変更がある場合）

### 2. デプロイ状態の確認

GitHub Pagesの設定ページで、以下のように表示されるはずです：

```
Your site is live at https://kmh-no3.github.io/game_901/
```

もし「Your site is ready to be published」と表示されている場合は、「Save」をクリックして公開してください。

### 3. デプロイの待機時間

- 初回デプロイ: 5〜10分程度かかることがあります
- 更新後の反映: 1〜5分程度かかることがあります
- ブラウザのキャッシュをクリアして再度アクセスしてみてください

### 4. ファイルの確認

以下のファイルがルートディレクトリに存在することを確認：
- ✅ `index.html`
- ✅ `game.js`
- ✅ 画像ファイル（reimu.png, marisa.png, moon.png, castle.png）

### 5. ブランチの確認

現在、`main`ブランチが使用されています。GitHub Pagesの設定で「main」ブランチを選択してください。

## 解決手順（ステップバイステップ）

1. **GitHubリポジトリにアクセス**
   - https://github.com/kmh-no3/game_901

2. **Settings → Pages に移動**

3. **Source セクションで以下を設定**
   - Branch: `main`
   - Folder: `/ (root)`

4. **Save をクリック**

5. **数分待つ（5〜10分）**

6. **再度アクセス**
   - https://kmh-no3.github.io/game_901/
   - ブラウザのキャッシュをクリア（Cmd+Shift+R または Ctrl+Shift+R）

## よくある問題

### 問題: 「Your site is ready to be published」と表示される
**解決策**: 「Save」ボタンをクリックして公開してください。

### 問題: ブランチが「master」になっている
**解決策**: ブランチを「main」に変更してください（既に`main`ブランチを作成済みです）。

### 問題: 404エラーが続く
**解決策**: 
- デプロイログを確認（Settings → Pages → 「View deployment」）
- エラーメッセージを確認
- ファイル名の大文字・小文字を確認（`Index.html`ではなく`index.html`）

## 確認用コマンド

ローカルで以下のコマンドを実行して、ファイルが正しくコミットされているか確認：

```bash
git ls-files | grep -E "(index\.html|game\.js)"
```

すべてのファイルが表示されれば問題ありません。

