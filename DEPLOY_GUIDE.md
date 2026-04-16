# 🚀 Yasu Tabi デプロイ手順書

## 📦 ファイル一覧

GitHubにアップロードするファイル：

```
yasutabi/
├── index.html          ← メインのLP（SEO・OGP対応済み）
├── og-image.png        ← SNSシェア時の画像（1200x630）
├── robots.txt          ← 検索エンジン用
├── sitemap.xml         ← SEO用
└── README.md           ← GitHubリポジトリの説明
```

---

## ステップ1：GitHubにファイルをアップロード

### ❶ 既存のリポジトリにアクセス
GitHub の Yasu Tabi リポジトリを開く

### ❷ ファイルをアップロード
1. 「Add file」→「Upload files」をクリック
2. 5つのファイルを全部ドラッグ&ドロップ：
   - `index.html`
   - `og-image.png`
   - `robots.txt`
   - `sitemap.xml`
   - `README.md`
3. 下のコミットメッセージ欄に：`Initial LP deployment with SEO and OGP`
4. 「Commit changes」をクリック

### ❸ Cloudflare Pages が自動デプロイ
接続済みなので、プッシュ後 **30秒〜1分** で自動で反映されます。

**確認URL：** `https://yasutabi.pages.dev/`（プロジェクト名によって異なる）

✅ スマホでも確認してみてください！

---

## ステップ2：Formspree設定（メアド収集）

### ❶ アカウント作成
👉 https://formspree.io/register

- メールアドレスとパスワードで登録
- メール認証を完了

### ❷ フォーム作成
1. ダッシュボードで「+ New Form」をクリック
2. 以下を入力：
   - **Form name**: `Yasu Tabi 事前登録`
   - **Send emails to**: きのこさんのメアド
3. 「Create Form」クリック

### ❸ エンドポイントURLをコピー
フォーム作成後、以下のような形のURLが表示されます：
```
https://formspree.io/f/abcd1234
```

この `abcd1234` の部分（フォームID）を私に教えてください。**index.htmlを更新します。**

または、ご自身でやる場合：
- `index.html` の中の `YOUR_FORM_ID` を検索
- その部分をフォームIDに置き換え
- GitHubに再アップロード → 自動デプロイ

### ❹ 動作テスト
公開URLでフォームにメールアドレスを入力 → 送信
- きのこさんのメアドにテスト通知が届く
- Formspreeダッシュボードに送信データが表示される

---

## ステップ3：楽天ウェブサービス登録

### ❶ 楽天会員ログイン
👉 https://webservice.rakuten.co.jp/

楽天IDでログイン（通販で使っているアカウントでOK）

### ❷ アプリ登録
1. 「新規アプリ登録」をクリック
2. 以下を入力：

| 項目 | 入力内容 |
|---|---|
| アプリ名 | Yasu Tabi |
| アプリURL | https://yasutabi.pages.dev （公開URL） |
| コールバック許可ドメイン | yasutabi.pages.dev |
| アプリの説明 | AIが旅行プランを自動作成するWebアプリ |

3. 規約に同意して登録

### ❸ 取得する情報（安全な場所にメモ）
登録後、以下を控えてください：
- **applicationId**（アプリID / 20桁の数字）
- **affiliateId**（アフィリエイトID / 英数字混合）※楽天アフィリエイトからも取得可

👉 **楽天アフィリエイト**: https://affiliate.rakuten.co.jp/

### ❹ API制限の確認
- 1秒に1リクエストまで
- 1日の上限なし
- MVPには十分な無料枠

---

## ステップ4：バリューコマース審査申請

### ❶ パートナー登録
👉 https://www.valuecommerce.ne.jp/

「無料パートナー登録」をクリック

### ❷ サイト情報を入力

| 項目 | 入力内容 |
|---|---|
| サイトURL | https://yasutabi.pages.dev |
| サイト名 | Yasu Tabi |
| サイトジャンル | 旅行 |
| 月間PV | 〜1,000（正直に） |
| サイト説明 | AIが楽天・Yahoo!・一休の最安値を比較する旅行プランナー |

### ❸ 個人情報入力
- 氏名
- 住所（報酬振込用）
- 銀行口座
- 電話番号

### ❹ 審査待ち（通常1〜5営業日）
審査通過後、以下と「広告プログラム提携申請」：
- **Yahoo!トラベル**
- **一休.com**
- **じゃらんnet**（予備）

**⚠️ 審査のコツ：**
- LPが**公開されている状態**で申請
- サイトに**ある程度のコンテンツ**がある方が通りやすい
- プライバシーポリシーがあるとベター（後で追加）

---

## ステップ5：SNSアカウント開設

### ❶ X（Twitter）

**ユーザー名候補（使えるものを選ぶ）：**
- `@yasutabi_jp`
- `@yasutabi_ai`
- `@yasutabi_app`

**プロフィール文（コピペ用）：**
```
🌊 安い旅をAIが見つける「Yasu Tabi」公式

楽天・Yahoo!・一休の最安値を横断比較
駐車場・営業時間まで含む旅行プランを自動作成

まもなくリリース ⬇️ 事前登録はこちら
https://yasutabi.pages.dev
```

**ヘッダー画像**：og-image.png をそのまま使える

**初回投稿例：**
```
🎉 Yasu Tabiの開発をはじめました

「安い宿を3サイトで比較するの面倒」
「飲食店の駐車場、いつもわからない」

そんな旅行の面倒をAIで解決する
Webアプリを作っています✍️

まもなくリリース、事前登録は👇
https://yasutabi.pages.dev

#旅行好きと繋がりたい #旅行
```

### ❷ Instagram

**ユーザー名候補：**
- `@yasutabi.travel`
- `@yasutabi_app`

**プロフィール文：**
```
🌊 AIが見つける、いちばん安い旅
📸 きのこの旅行記 × 旅行プランナー
⬇️ 事前登録＆詳細はこちら
```

**投稿戦略（一眼レフ写真資産を活用）：**
- 過去の旅行写真をLightroomで仕上げ直して投稿
- キャプションで「この温泉の駐車場は〇台」「入口はここ」など実用情報
- ハッシュタグ：`#国内旅行 #温泉旅行 #旅行好きと繋がりたい #カメラ好きな人と繋がりたい`

---

## ✅ Phase A 完了チェックリスト

```
□ index.html ほか5ファイルをGitHubにアップロード
□ Cloudflare Pages で公開確認（yasutabi.pages.dev）
□ スマホで表示確認
□ Formspreeアカウント作成
□ フォームID取得 → index.html に反映
□ 事前登録フォーム実際にテスト（メール受信確認）
□ 楽天ウェブサービス アプリID取得
□ 楽天アフィリエイトID取得
□ バリューコマース審査申請
□ Xアカウント開設＆初回投稿
□ Instagramアカウント開設
```

---

## 次回の作業（Phase B：MVP開発）

Phase A が完了したら、楽天トラベルAPIの接続テストから始めます。Cloudflare Workersでサーバーレス関数を書いて、AIプラン生成を実装します。

**Phase B 開始前に必要なもの：**
- 楽天 applicationId
- 楽天 affiliateId
- Anthropic API Key（Claude API用、有料 $5〜チャージ必要）
- Google Places API Key（$200/月 無料枠あり）

---

## 💬 質問・詰まったら

各ステップで困ったら以下を教えてください：
- エラーメッセージのスクショ or テキスト
- どのステップの何番で詰まったか
- 表示されている画面の状態
