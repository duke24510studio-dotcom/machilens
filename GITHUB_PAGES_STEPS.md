# GitHub Pagesで公開する手順

## 1. GitHubでリポジトリを作る

1. `https://github.com/new` を開く。
2. Repository name に `machilens` などを入力する。
3. Public を選ぶ。
4. `Add a README file` はオフでOK。
5. `Create repository` を押す。

## 2. ローカルからpushする

GitHubの新規リポジトリ画面に出るURLを使います。

例:

```powershell
cd C:\Users\satos\Downloads\machilens_cloudflare_upload
git remote add origin https://github.com/あなたのユーザー名/machilens.git
git branch -M main
git push -u origin main
```

## 3. GitHub Pagesを有効化する

1. GitHubのリポジトリを開く。
2. `Settings` を開く。
3. 左メニューの `Pages` を開く。
4. `Build and deployment` の `Source` で `Deploy from a branch` を選ぶ。
5. Branch を `main`、Folder を `/root` にする。
6. `Save` を押す。

## 4. 公開URLを確認する

数分待つと、Pages画面にURLが表示されます。

例:

```text
https://あなたのユーザー名.github.io/machilens/
```

GitHub公式ドキュメントでは、公開まで最大10分ほどかかる場合があります。

## よくあるつまずき

- トップが404になる: `index.html` がリポジトリ直下にあるか確認。
- ロゴが出ない: `assets` フォルダがリポジトリ直下にあるか確認。
- 変更が反映されない: Pagesの反映に数分かかるので待つ。
- リポジトリがPrivate: 無料プランではPublicの方が確実。
