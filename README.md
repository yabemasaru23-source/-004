# レディースキッド — 靴診断LP

お手持ちの靴 評価・仕分けアドバイス サービス ランディングページ

## 📁 ファイル構成

```
ladieskid/
├── index.html              ← LP本体（SEO・GA4・OGP設定済み）
├── README.md               ← このファイル（GitHub公開手順）
├── .gitignore
└── assets/
    └── images/
        ├── hero.jpg        ← FVメイン画像（靴擦れ・下駄箱・悩む女性）
        └── ogp.jpg         ← SNSシェア用OGP画像（1200×630px）
```

## 🚀 GitHub Pages でのデプロイ手順

```bash
# 1. リポジトリ初期化
git init
git add .
git commit -m "Initial commit: ladieskid LP"

# 2. GitHubへpush
git remote add origin https://github.com/<your-username>/<repo-name>.git
git push -u origin main
```

**GitHub上での設定：**
1. リポジトリの **Settings** → **Pages**
2. **Source**: `Deploy from a branch`
3. **Branch**: `main` / `(root)` → **Save**
4. 数分後に `https://<your-username>.github.io/<repo-name>/` で公開

## ✅ デプロイ前チェックリスト

### Google Analytics 4
- [ ] `GA_MEASUREMENT_ID` を実際の測定ID（**G-XXXXXXXXXX**）に書き換える
  - 場所：`index.html` の `<head>` 内、**2箇所**

### SEO・OGP
- [ ] `<link rel="canonical">` → 実際のURLに変更
- [ ] `og:url` → 実際のURLに変更
- [ ] `og:image` / `twitter:image` → 実際のOGP画像URLに変更
- [ ] JSON-LD 構造化データ → 店舗情報（住所・電話番号）を追記

### コンテンツ（赤字部分）
- [ ] 所要時間 `〇〇分` → 実際の時間に変更
- [ ] 料金 `〇〇,〇〇〇円（税込）` → 実際の料金に変更
- [ ] 上限足数の記載を追加（例：「※上限10足まで」）
- [ ] お客様事例テキストを実際の事例に変更
- [ ] `© 2025` の年号確認

### 画像（assets/images/ に追加）
- [ ] `hero.jpg` → FVメイン画像（靴擦れ or 下駄箱 or 悩む女性）
  - 推奨サイズ：1200×900px 以上
- [ ] `ogp.jpg` → SNSシェア用（1200×630px）
- HTMLの `<!-- 実際の画像: <img ...> -->` コメントアウトを解除

## 📊 GA4 イベント計測

以下のCTAクリックが自動で計測されます：

| イベント名 | ラベル | 計測箇所 |
|---|---|---|
| `click_cta` | `header` | ヘッダーの予約ボタン |
| `click_cta` | `hero` | ヒーローセクションのCTA |
| `click_cta` | `cta_bottom` | ページ下部のCTAセクション |

GA4管理画面 → **レポート** → **イベント** で確認できます。

## 🔍 SEO推奨対応

- [ ] **Google Search Console** にサイトを登録
- [ ] **sitemap.xml** を作成してSearch Consoleに送信（単ページの場合は任意）
- [ ] ページ表示速度を **PageSpeed Insights** で確認
- [ ] 実際の画像に `alt` テキストが適切に設定されているか確認

## 🎨 カスタマイズ

### カラー変更
`index.html` 内の `:root` CSS変数を編集：
```css
--primary: #7B5C3E;       /* メインブラウン */
--accent:  #C8A882;       /* アクセントベージュ */
```

### バイオメカニクス図解
`strength-card` 内の `.biomech-visual` 部分に、足の骨格図・屈曲点イラストを追加することで専門性の訴求力が向上します。

### 仕分けボックスアイコン
emoji の代わりに SVG アイコンを使うと、より洗練された印象になります。
