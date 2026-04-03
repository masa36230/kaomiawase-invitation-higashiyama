# お顔合わせのご案内（静的LP）

GitHub Pages 用の静的LPです。トップURLは `index.html`、同一内容の別名ファイルは `invitation_higashiyama.html`（`/invitation_higashiyama.html` でも開けます）。

## 公開手順（初回）

1. ターミナルで GitHub CLI にログインする  
   `gh auth login`  
   （ブラウザ認証で問題ありません）

2. このフォルダで次を実行する  
   `bash publish_github_pages.sh`

3. スクリプトが表示する `https://<ユーザー名>.github.io/<リポジトリ名>/` を開く（反映まで1〜3分かかることがあります）

## HTML の更新

`index.html`（および同内容の `invitation_higashiyama.html`）を編集後:

```bash
git add index.html invitation_higashiyama.html
git commit -m "Update invitation page"
git push
```

数分後にサイトへ反映されます。

## Pages の URL に「12」などを含めたくない場合

GitHub Pages のユーザー向けURLは次の形で、**先頭のユーザー名は GitHub アカウントのログイン名**です。

`https://<GitHubユーザー名>.github.io/<リポジトリ名>/`

- **リンクはユーザー名を変えれば変わります。** リポジトリ名だけ変えても、`*.github.io` の左側はアカウント名のままです。
- **対処1（推奨）**: GitHub にログイン → **Settings（設定）** → **Account** → **Change username** で、使いたい名前（例: `masafumi` や `masakaitsu`）に変更する。利用可能な名前のみ登録できます。変更後のURLは `https://<新ユーザー名>.github.io/<リポジトリ名>/` になります。しばらく旧URLからのリダイレクトが効くことがありますが、**共有リンクは新URLに差し替える**のが確実です。
- **対処2**: 別アカウント（名前に数字を含めない）でリポジトリを作り直し、このフォルダを push し直す。
- **対処3**: 独自ドメインを当てる（Pages の Custom domain）。`example.com` ならユーザー名はURLに出ません。

エージェント側からアカウント名の変更は実行できないため、上記は GitHub の画面またはご自身のターミナルで実施してください。
