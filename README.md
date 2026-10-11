# URINOA Public Site

URINOA（ウリノア）の公開用静的Webサイトです。

## Files

- `index.html` — Support
- `privacy.html` — Privacy Policy
- `terms.html` — Terms of Use
- `legal.html` — 特定商取引法に基づく表記
- `styles.css` — Shared styles
- `.nojekyll` — GitHub Pages用

外部ライブラリ、ビルド処理、JavaScriptは使用していません。ファイルをリポジトリ直下へ置くだけでGitHub Pagesから公開できます。

## Local preview

このディレクトリで次を実行します。

```sh
python3 -m http.server 4174
```

ブラウザで `http://127.0.0.1:4174/` を開きます。

## Publish with GitHub Pages

1. GitHubで公開用リポジトリを新規作成します（例：`urinoa-support`）。
2. このディレクトリ内の全ファイルをリポジトリ直下へ追加し、`main`ブランチへpushします。
3. GitHubのリポジトリで **Settings → Pages** を開きます。
4. **Build and deployment** のSourceで **Deploy from a branch** を選択します。
5. Branchを **main**、フォルダを **/(root)** にして保存します。
6. Pagesの公開完了後、表示されたHTTPS URLを確認します。

リポジトリ名が `urinoa-support` の場合、一般的なURL形式は次のとおりです。

```text
Support: https://<GitHubユーザー名>.github.io/urinoa-support/
Privacy: https://<GitHubユーザー名>.github.io/urinoa-support/privacy.html
Terms:  https://<GitHubユーザー名>.github.io/urinoa-support/terms.html
Legal:  https://<GitHubユーザー名>.github.io/urinoa-support/legal.html
```

実際のURLはGitHub Pages画面に表示されたものを使用してください。

## Connect to the iOS app

公開後、URINOAアプリのApp Store用環境設定へ次を設定します。

```text
VITE_PRIVACY_POLICY_URL=<公開したPrivacy URL>
VITE_TERMS_URL=<公開したTerms URL>
```

App Store Connectには次を設定します。

- Privacy Policy URL: `privacy.html` の公開URL
- Support URL: `index.html` の公開URL
- Terms of Use: `terms.html` の公開URL（必要なメタデータ欄または説明文）
- 特定商取引法に基づく表記: `legal.html` の公開URL。アプリ内の購入導線または法務情報から容易に確認できる状態にします。

## 特定商取引法に基づく開示請求の運用

`legal.html` では、消費者庁「通信販売広告Q&A」Q15〜Q18の考え方を踏まえ、住所・電話番号について開示請求方式を採用しています。この方式は、ページに文言を掲載するだけでは足りません。

- `proto.apps.support@gmail.com` 宛ての「特商法に基づく開示請求」を確実に受信・確認できる状態にします。
- 購入申込みの意思決定に先立って十分な時間的余裕をもって確認できるよう、請求を受けた場合は遅滞なく、正確な住所・電話番号を電子メール等で開示します。
- 開示する住所は現に活動している正確な住所、電話番号は確実に連絡できる番号とします。
- 迷惑メール振り分けや長期不在により請求を見落とさない運用を用意します。
- この運用を維持できない場合は、`legal.html` に正確な住所・電話番号を直接表示する必要があります。

公開前に、実際の事業形態へ適合しているか専門家へ確認することを推奨します。

## Contact information

- Development brand: PROTO Apps
- Operator: Sakuragawa Kazuki
- Email: proto.apps.support@gmail.com
