# J Coaching website

J Coachingの日本語コーチング紹介サイト。公開中の最新版から引き継いだ、GitHub管理用のソース一式です。

| 項目 | 内容 |
| --- | --- |
| GitHub | https://github.com/Jcoaching/jcoaching-website |
| 現在の公開先 | https://j-coaching.sota27310726.chatgpt.site |
| 独自ドメイン | jcoaching.jp（取得済み、接続は確認待ち） |
| 構成 | HTML5 / CSS3 / Vanilla JavaScript / WebP |
| 言語 | 英語が初期表示。日本語切り替えあり |
| フレームワーク・依存パッケージ | なし |
| ビルド | 不要。`dist/`が編集対象であり、公開用ファイルでもある |
| バックエンド・DB・APIキー | なし |

## ローカルで確認する

Python 3がある環境で、このREADMEのあるディレクトリから実行します。

```sh
python3 -m http.server 8000 --bind 127.0.0.1 --directory dist
```

ブラウザで `http://localhost:8000` を開きます。ファイルのダブルクリックではなく、HTTPで配信してください。CSS・JS・画像は `/assets/...` などのルート相対パスを使っています。

## 編集するファイル

| ファイル | 内容 |
| --- | --- |
| `dist/index.html` | ページ構成、英語本文、相談・SNSリンク、画像の表示範囲 |
| `dist/styles.css` | 配色、書体、余白、スマホ対応、アニメーション |
| `dist/app.js` | 日本語訳、言語切り替え、メニュー、月別タブ、動画再生 |
| `dist/assets/` | 公開用のWebP画像14点 |
| `HANDOFF.md` | 引き継ぎ事項、素材の扱い、ドメイン設定、確認項目 |
| `SHA256SUMS` | 引き継ぎ時点のサイトファイル17点のハッシュ |

## GitHubから取得する

このリポジトリはPrivateです。管理者からアクセス権を受け取った後、担当者のGitHub認証が設定された環境で取得してください。

```sh
git clone https://github.com/Jcoaching/jcoaching-website.git
cd jcoaching-website
```

その後、上記のローカル確認コマンドで起動できます。担当者を追加する際は、このリポジトリのSettingsからCollaboratorsを開き、GitHubユーザー名を指定して招待してください。

過去のSitesのGit履歴は移していません。現在掲載している画像とソースで管理を始めています。元のSitesリポジトリとGitHubの自動同期は設定していません。

## 公開する

ドキュメントルートに `dist/` の中身を配置する静的ホスティングに対応します。ビルドコマンドや環境変数は不要です。

`/repository-name/` のようなサブパスで配信すると、ルート相対の画像・CSS・JSが参照できません。独自ドメインのルートで配信するか、パスの調整が必要です。

既存サイトの公開先はChatGPT Sitesです。GitHubへのpushだけで既存サイトが更新される設定はありません。運用するホスティングとデプロイ方法は引き継ぎ時に決めてください。

## 引き継ぎ元

- 取得日：2026年9月15日
- 公開バージョン：5
- 元ソースのコミット：`38f5fcaba89053d0614f37a1a2d4f0502745a9e4`
- `dist/` 内の17ファイルは元ソースとバイト単位で同一です。
- 所有者提供の素材を含みます。公開用オープンソースライセンスは付与していません。
