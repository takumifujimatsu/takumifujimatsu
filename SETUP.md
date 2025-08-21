# GitHub プロフィールページの設定方法

## 📋 概要

このリポジトリは、GitHub のプロフィールページを作成するためのテンプレートです。美しいデザインと動的なコンテンツを含むプロフィールページを作成できます。

## 🚀 セットアップ手順

### 1. リポジトリの作成

1. GitHub で新しいリポジトリを作成
2. リポジトリ名を **あなたの GitHub ユーザー名** と同じにする
   - 例: ユーザー名が `john-doe` の場合、リポジトリ名も `john-doe`
3. リポジトリを **Public** にする
4. README.md ファイルを追加する

### 2. ファイルのカスタマイズ

#### README.md の編集

1. `README.md` ファイルを開く
2. 以下の項目を自分の情報に変更：
   - `[あなたの名前]` → 実際の名前
   - `YOUR_USERNAME` → 実際の GitHub ユーザー名
   - プロジェクトのリンク
   - 連絡先情報
   - 技術スタック

#### 技術スタックのカスタマイズ

使用している技術に合わせて、バッジを追加・削除してください：

```markdown
![技術名](https://img.shields.io/badge/-技術名-色コード?style=flat-square&logo=ロゴ名&logoColor=white)
```

### 3. GitHub Actions の設定（オプション）

#### WakaTime 統計の追加

1. [WakaTime](https://wakatime.com/) にアカウントを作成
2. API キーを取得
3. GitHub リポジトリの Settings → Secrets and variables → Actions
4. 新しいシークレットを追加：
   - 名前: `WAKATIME_API_KEY`
   - 値: WakaTime の API キー

#### 手動実行

GitHub Actions ワークフローを手動で実行する場合：

1. リポジトリの Actions タブに移動
2. "Update GitHub Profile" ワークフローを選択
3. "Run workflow" ボタンをクリック

### 4. カスタム HTML ページの使用（オプション）

`profile.html` ファイルを GitHub Pages で公開する場合：

1. リポジトリの Settings → Pages
2. Source を "Deploy from a branch" に設定
3. Branch を "main" に設定
4. フォルダを "/ (root)" に設定
5. Save をクリック

## 🎨 カスタマイズのヒント

### 色の変更

HTML ファイルの CSS で色を変更できます：

```css
:root {
  --primary-color: #667eea;
  --secondary-color: #764ba2;
  --text-color: #2d3748;
}
```

### アニメーションの追加

CSS アニメーションを追加して、より魅力的なプロフィールページにできます：

```css
@keyframes fadeIn {
  from {
    opacity: 0;
    transform: translateY(20px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

.profile-card {
  animation: fadeIn 0.8s ease-out;
}
```

### 新しいセクションの追加

README.md に新しいセクションを追加できます：

```markdown
## 🏆 受賞歴

- 2023 年: ベストデベロッパー賞
- 2022 年: イノベーション賞

## 📚 執筆活動

- [技術ブログ記事 1](リンク)
- [技術ブログ記事 2](リンク)
```

## 📊 統計の追加

### GitHub 統計

GitHub 統計を追加するには、以下の URL を使用：

```
https://github-readme-stats.vercel.app/api?username=YOUR_USERNAME&show_icons=true&theme=radical
```

### 言語統計

使用言語の統計を追加：

```
https://github-readme-stats.vercel.app/api/top-langs/?username=YOUR_USERNAME&layout=compact&theme=radical
```

### 貢献グラフ

貢献グラフを追加：

```
https://github-readme-streak-stats.herokuapp.com/?user=YOUR_USERNAME&theme=radical
```

## 🔧 トラブルシューティング

### 統計が表示されない

1. リポジトリが Public になっているか確認
2. GitHub ユーザー名が正しいか確認
3. キャッシュをクリアしてページを再読み込み

### GitHub Actions が動作しない

1. リポジトリの Settings → Actions → General
2. "Allow all actions and reusable workflows" を選択
3. ワークフローファイルの構文を確認

### 画像が表示されない

1. 画像の URL が正しいか確認
2. 画像が Public にアクセス可能か確認
3. 代替画像サービスを使用

## 📝 ベストプラクティス

1. **定期的な更新**: プロフィール情報を定期的に更新
2. **プロジェクトの追加**: 新しいプロジェクトを追加してポートフォリオを充実
3. **技術スタックの更新**: 新しい技術を学んだら技術スタックに追加
4. **統計の活用**: GitHub 統計を活用して活動を可視化
5. **レスポンシブデザイン**: モバイルデバイスでも見やすいデザインにする

## 🤝 貢献

このテンプレートの改善提案やバグ報告は、Issue または Pull Request でお知らせください。

## 📄 ライセンス

このプロジェクトは MIT ライセンスの下で公開されています。

---

⭐ このテンプレートが役に立ったら、スターを押してください！
