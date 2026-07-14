# UNEPLAGE/morakniv-jp

モーラナイフ ブランドポータル **https://morakniv.jp** の公開用リポジトリ。

- **運用**: GitHub Organization **UNEPLAGE** 配下。ホスティングは **Vercel**（このリポジトリの `main` に push すると自動デプロイ）。
- **このリポジトリの中身 = 完成HTML（デプロイ対象）**。純粋な静的サイト（ビルド不要 / Vercel Framework Preset = Other）。

## ブランチ
- `main` … 本番（morakniv.jp）。パスワード無し・検索許可。
- `preview` … 確認用。パスワードゲート有り（パス: `upiupi`）・noindex。
  - プレビューURL: `https://morakniv-jp-git-preview-upi-s-projects.vercel.app`

## 編集はこのリポジトリでは行いません
編集用の「元ファイル（`index_src.html` / `assets/` / `build.py`）」は **Google Drive 共有フォルダ** にあります（画像込みで大きいため）。
編集フロー・仕様・アカウント情報は、その共有フォルダ内の以下を参照:
- `HANDOFF_引き継ぎ.md` … 全体の運用・仕様
- `README_ソース.md` … ビルド手順
- `MEMBER_SETUP.md` … 新メンバーのセットアップ

## 反映フロー（概要）
1. Google Drive の `index_src.html` 等を編集
2. `build.py` で `prod/`（本番用）と `preview/`（確認用）を生成
3. `preview/` を **preview** ブランチへ → プレビューで確認（`upiupi`）
4. OKなら `prod/` を **main** へ → 本番反映

## 触ってはいけないファイル
- `favicon.ico`
- `google2a768b3a3d5d7f0f.html`（Google Search Console 所有権確認）
- 各ページの GA4 タグ / ストアリンクの UTM パラメータ

## インフラ情報
- ドメイン: `morakniv.jp`（お名前.com。NS=01〜04.dnsv.jp、A `@`→216.198.79.1=Vercel）
- 計測: GA4 `G-F83W782HB8`（morakniv.jp でのみ計測）
- 送客先: Shopify `store.upioutdoor.com`（UTMで流入計測）

<!-- deploy check: UNEPLAGE org 2026-07-14 -->
