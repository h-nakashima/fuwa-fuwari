# 🍥fuwa-fuwari (fuwari customized by h-nakashima)

[Astro](https://astro.build) で構築された静的ブログテンプレート。h-nakashimaによるカスタマイズ版。

[**🖥️ライブデモ (Cloudflare Pages)**](https://fuwari-template.pages.dev)&nbsp;&nbsp;&nbsp;/&nbsp;&nbsp;&nbsp;
[**📦オリジナルバージョン**](https://github.com/saicaca/fuwari)&nbsp;&nbsp;&nbsp;/&nbsp;&nbsp;&nbsp;

> README バージョン：`2024-09-01` 

![Preview Image](./sample_home.png)

## ✨ 特徴
### オリジナルリポジトリ
- [x] [Astro](https://astro.build) 及び [Tailwind CSS](https://tailwindcss.com) で構築
- [x] スムーズなアニメーションとページ遷移
- [x] ライト/ダークテーマ対応
- [x] カスタマイズ可能なテーマカラーとバナー
- [x] レスポンシブデザイン
- [ ] コメント機能
- [x] 検索機能
- [ ] 目次

### 本リポジトリの追加機能
- [x] サイドバーを右側へ移動
- [x] サイドバーへ最近の投稿ウィジェットを追加
- [x] Google Analytics 対応
- [ ] ページごとの閲覧数カウンター
- [ ] サイドバーへアクセスランキングを追加
- [ ] Google Adsense 対応

## 🚀 使用方法

1. [テンプレート](https://github.com/h-nakashima/fuwa-fuwari/generate)から新しいリポジトリを作成するかCloneをします。
2. ブログをローカルで編集するには、リポジトリをクローンした後、`pnpm install` と `pnpm add sharp` を実行して依存関係をインストールします。  
   - [pnpm](https://pnpm.io) がインストールされていない場合は `npm install -g pnpm` で導入可能です。
3. `src/config.ts` ファイルを編集する事でブログを自分好みにカスタマイズ出来ます。
4. `pnpm new-post <filename>` で新しい記事を作成し、`src/content/posts/`.フォルダ内で編集します。
5. 作成したブログをVercel、Netlify、GitHub Pagesなどにデプロイするには[ガイド](https://docs.astro.build/ja/guides/deploy/)に従って下さい。加えて、別途デプロイを行う前に `astro.config.mjs` を編集してサイト構成を変更する必要があります。

### テンプレートの更新をクローンしたリポジトリに反映するには
#### 初回更新時
[テンプレート](https://github.com/h-nakashima/fuwa-fuwari/generate)の更新をクローンしたリポジトリに取り込み、`feature/template-sync` ブランチでPRを作成する方法を示します。

1. **新しいブランチを作成**
   テンプレートの変更を適用するための `feature/template-sync` ブランチをクローンしたリポジトリ内で作成します。
   ```bash
   git checkout -b feature/template-sync
   ```

2. **テンプレートリポジトリをリモートとして追加**
   テンプレートリポジトリ `git@github.com:h-nakashima/fuwa-fuwari.git` をリモートとして追加します。
   ```bash
   git remote add template git@github.com:h-nakashima/fuwa-fuwari.git
   ```

3. **テンプレートリポジトリの変更をフェッチ**
   テンプレートリポジトリの最新の変更を取得します。
   ```bash
   git fetch template
   ```

4. **テンプレートリポジトリの変更をクローンしたリポジトリにマージ**
   テンプレートリポジトリの `main` ブランチの最新の変更を `feature/template-sync` ブランチにマージします。
   ```bash
   git merge template/main --allow-unrelated-histories
   ```

   コンフリクトが発生した場合は、手動で解決し、マージを完了させます。

5. **変更をコミット**
   コンフリクトを解消した後、必要に応じて変更を確認し、コミットします。
   ```bash
   git commit -m "Merged updates from template repository"
   ```

6. **ブランチをリモートにプッシュ**
   `feature/template-sync` ブランチをプッシュします。
   ```bash
   git push origin feature/template-sync
   ```

7. **GitHubでプルリクエストを作成**
   GitHub上で、クローンしたリポジトリの `feature/template-sync` ブランチに対してプルリクエストを作成します。プルリクエストのタイトルや説明を適切に記入し、テンプレートリポジトリからの変更内容が反映されるようにします。

#### 2回目以降の更新時

1. **ブランチ切り替え**
   テンプレートの変更を適用するための `feature/template-sync` に切り替えます。
   ```bash
   git checkout feature/template-sync
   ```

2. **テンプレートリポジトリの変更をフェッチ**
   テンプレートリポジトリの最新の変更を取得します。
   ```bash
   git fetch template
   ```

4. **テンプレートリポジトリの変更をクローンしたリポジトリにマージ**
   テンプレートリポジトリの `main` ブランチの最新の変更を `feature/template-sync` ブランチにマージします。
   ```bash
   git merge template/main
   ```

   コンフリクトが発生した場合は、手動で解決し、マージを完了させます。

5. **変更をコミット**
   コンフリクトを解消した後、必要に応じて変更を確認し、コミットします。
   ```bash
   git commit -m "Merged updates from template repository"
   ```

6. **ブランチをリモートにプッシュ**
   `feature/template-sync` ブランチをプッシュします。
   ```bash
   git push
   ```

7. **GitHubでプルリクエストを作成**
   GitHub上で、クローンしたリポジトリの `feature/template-sync` ブランチに対してプルリクエストを作成します。プルリクエストのタイトルや説明を適切に記入し、テンプレートリポジトリからの変更内容がクローンしたリポジトリに反映されるようにします。

## ⚙️ 記事のフロントマター

```yaml
---
title: My First Blog Post
published: 2023-09-09
description: This is the first post of my new Astro blog.
image: /images/cover.jpg
tags: [Foo, Bar]
category: Front-end
draft: false
---
```

## 🧞 コマンド

すべてのコマンドは、ターミナルでプロジェクトのルートから実行する必要があります:

| Command                             | Action                                      |
|:------------------------------------|:--------------------------------------------|
| `pnpm install` AND `pnpm add sharp` | 依存関係のインストール                                 |
| `pnpm clean`                        | ビルド出力とキャッシュを削除                             |
| `pnpm dev`                          | `localhost:4321` で開発用ローカルサーバーを起動            |
| `pnpm build`                        | `./dist/` にビルド内容を出力                         |
| `pnpm preview`                      | デプロイ前の内容をローカルでプレビュー                         |
| `pnpm new-post <filename>`          | 新しい投稿を作成                                    |
| `pnpm astro ...`                    | `astro add`, `astro check` の様なコマンドを実行する際に使用 |
| `pnpm astro --help`                 | Astro CLIのヘルプを表示                            |
