# WorkStyle Insight

公開サイト: https://workstyle-insight.tokyo/

## 更新するファイル

- `index.html`: 公開中の記事。移行前のHTMLをそのまま保持しています。
- `article-draft.html`: 新記事の下書き。経歴・実績・口コミ・運営者情報を確認するまで `noindex` を維持してください。
- `CNAME`: 独自ドメイン設定。変更・削除しないでください。
- `.nojekyll`: 静的HTMLとして配信するための設定。

## 更新方法

GitHubで `index.html` を開き、Edit this fileから編集し、Commit changesで `main` に保存します。GitHub Pagesが自動で公開に反映します。処理状況はActionsで確認できます。

HTMLはUTF-8で保存し、`<meta charset="UTF-8">` を維持してください。GitHub Pagesは `Content-Type: text/html; charset=utf-8` で配信します。Cloudflare用の `_headers` やApache用の `.htaccess` は不要です。

## ホスティング

GitHub Pages: mainブランチのルートを公開。
Cloudflare: DNS管理とwwwから正式URLへの転送。`@` は `factlabcontact.github.io` を指すCNAME（DNS only）。ルートのCNAMEはCloudflareによりフラット化されます。`www` は同じ接続先のCNAME（Proxied）で、Single Redirectによりパス・クエリを維持して `https://workstyle-insight.tokyo/` へ301転送します。本文はGitHub Pagesが配信します。

HTTPS証明書とHTTPからHTTPSへの転送を有効化済みです。

## 新記事の公開

下書きの未確認箇所を実際の情報に差し替え、掲載同意のある口コミのみを使用してください。内容確認後に `index.html` へ反映し、準備中の案内と `noindex` を削除します。
