# 🛠️ GitHub プロフィール用の人気ツール集

このドキュメントでは、GitHub プロフィールページをより魅力的にするために使用できる有志が開発したツールを紹介します。

## 📊 統計・分析ツール

### 1. GitHub Readme Stats

**URL**: https://github.com/anuraghazra/github-readme-stats

最も人気のある GitHub 統計カード生成ツールです。

```markdown
<!-- 基本的な統計カード -->

![GitHub Stats](https://github-readme-stats.vercel.app/api?username=YOUR_USERNAME&show_icons=true&theme=radical)

<!-- 言語統計 -->

![Top Languages](https://github-readme-stats.vercel.app/api/top-langs/?username=YOUR_USERNAME&layout=compact&theme=radical)

<!-- カスタムテーマ -->

![GitHub Stats](https://github-readme-stats.vercel.app/api?username=YOUR_USERNAME&show_icons=true&theme=radical&hide_border=true&bg_color=0D1117&title_color=58A6FF&text_color=C9D1D9&icon_color=58A6FF)
```

### 2. GitHub Streak Stats

**URL**: https://github.com/DenverCoder1/github-readme-streak-stats

GitHub の連続コミット日数を表示します。

```markdown
![GitHub Streak](https://github-readme-streak-stats.herokuapp.com/?user=YOUR_USERNAME&theme=radical&hide_border=true)
```

### 3. GitHub Profile Trophy

**URL**: https://github.com/ryo-ma/github-profile-trophy

GitHub の実績をトロフィー形式で表示します。

```markdown
![GitHub Trophy](https://github-profile-trophy.vercel.app/?username=YOUR_USERNAME&theme=radical&no-frame=true&no-bg=true&margin-w=4&row=1&column=7)
```

### 4. Profile Views Counter

**URL**: https://github.com/antonkomarev/github-profile-views-counter

プロフィールページの閲覧回数をカウントします。

```markdown
![Profile Views](https://komarev.com/ghpvc/?username=YOUR_USERNAME&color=brightgreen&style=flat-square)
```

## 🎨 アニメーション・ビジュアルツール

### 5. GitHub Contribution Snake

**URL**: https://github.com/Platane/snk

GitHub の貢献グラフを蛇の形にしたアニメーションを生成します。

```markdown
![Snake Animation](https://github.com/YOUR_USERNAME/YOUR_USERNAME/blob/output/github-contribution-grid-snake.svg)
```

### 6. GitHub Activity Readme

**URL**: https://github.com/jamesgeorge007/github-activity-readme

最近の GitHub アクティビティを表示します。

```markdown
<!-- GitHub Actions で自動更新 -->
```

## ⏱️ 時間追跡ツール

### 7. WakaTime Stats

**URL**: https://github.com/anmol098/waka-readme-stats

WakaTime のデータを使用してコーディング時間を表示します。

```markdown
![WakaTime Stats](https://github-readme-stats.vercel.app/api/wakatime?username=YOUR_USERNAME&theme=radical)
```

### 8. WakaTime Profile

**URL**: https://github.com/athul/waka-readme

より詳細な WakaTime 統計を表示します。

```markdown
<!-- GitHub Actions で自動更新 -->
```

## 🎯 特殊効果ツール

### 9. GitHub Profile Summary Cards

**URL**: https://github.com/vn7n24fzkq/github-profile-summary-cards

プロフィールの詳細な統計をカード形式で表示します。

```markdown
![Profile Summary](https://github-profile-summary-cards.vercel.app/api/cards/profile-details?username=YOUR_USERNAME&theme=radical)
```

### 10. GitHub Profile 3D Contrib

**URL**: https://github.com/yoshi389111/github-profile-3d-contrib

3D 形式で GitHub の貢献を表示します。

```markdown
![3D Contrib](https://github-profile-3d-contrib.vercel.app/api?username=YOUR_USERNAME&theme=radical)
```

## 🔧 設定方法

### GitHub Actions での自動更新

```yaml
name: Update Profile

on:
  schedule:
    - cron: "0 0 * * *"
  workflow_dispatch:

jobs:
  update-readme:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4

      # GitHub Activity
      - name: Update GitHub Activity
        uses: jamesgeorge007/github-activity-readme@master
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
        with:
          COMMIT_MSG: "Update GitHub Activity"
          MAX_LINES: 5

      # WakaTime Stats
      - name: Update WakaTime Stats
        uses: anmol098/waka-readme-stats@master
        env:
          WAKATIME_API_KEY: ${{ secrets.WAKATIME_API_KEY }}
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
        with:
          SHOW_TITLE: "false"
          SHOW_LINE_OF_CODE: "true"
          SHOW_PROFILE_VIEWS: "true"
          SHOW_LANGUAGE: "true"
          SHOW_OS: "true"
          SHOW_PROJECTS: "true"
          SHOW_EDITORS: "true"
          SHOW_LOC_CHART: "true"
          SHOW_LANGUAGE_CHART: "true"
          SHOW_DAYS_OF_WEEK: "true"
          SHOW_OVERVIEW: "true"
          SHOW_SHORT_INFO: "true"

      # Snake Animation
      - name: Generate Snake Animation
        uses: Platane/snk@master
        id: snake-gif
        with:
          github_user_name: ${{ github.repository_owner }}
          svg_out_path: dist/github-contribution-grid-snake.svg

      # Push Changes
      - name: Push to GitHub
        uses: ad-m/github-push-action@master
        with:
          github_token: ${{ secrets.GITHUB_TOKEN }}
          branch: ${{ github.ref }}
```

### 必要なシークレット

1. **GITHUB_TOKEN**: 自動的に提供されます
2. **WAKATIME_API_KEY**: WakaTime から取得（オプション）

## 🎨 テーマカスタマイズ

### 利用可能なテーマ

- `radical` - ダークテーマ（推奨）
- `tokyonight` - トーキョーナイト
- `dracula` - ドラキュラ
- `cobalt` - コバルト
- `synthwave` - シンセウェーブ
- `highcontrast` - ハイコントラスト
- `dark` - ダーク
- `transparent` - 透明

### カスタムカラー

```markdown
![Stats](https://github-readme-stats.vercel.app/api?username=YOUR_USERNAME&bg_color=0D1117&title_color=58A6FF&text_color=C9D1D9&icon_color=58A6FF&hide_border=true)
```

## 📱 モバイル対応

すべてのツールはモバイルデバイスでも適切に表示されます。レスポンシブデザインが組み込まれています。

## 🔄 更新頻度

- **GitHub Stats**: リアルタイム
- **WakaTime Stats**: 毎日自動更新
- **Snake Animation**: 毎日自動更新
- **Activity Feed**: 毎日自動更新

## 🚀 パフォーマンス最適化

1. **画像の遅延読み込み**: 必要に応じて画像を遅延読み込み
2. **キャッシュ**: 統計データはキャッシュされます
3. **CDN**: すべてのツールは CDN 経由で配信されます

## 🤝 トラブルシューティング

### 統計が表示されない場合

1. リポジトリが Public になっているか確認
2. GitHub ユーザー名が正しいか確認
3. キャッシュをクリアしてページを再読み込み

### WakaTime が動作しない場合

1. WakaTime API キーが正しく設定されているか確認
2. WakaTime プラグインがインストールされているか確認
3. 十分なデータが蓄積されているか確認

### Snake Animation が生成されない場合

1. GitHub Actions が有効になっているか確認
2. ワークフローファイルの構文を確認
3. 十分な貢献データがあるか確認

## 📚 参考リンク

- [GitHub Readme Stats](https://github.com/anuraghazra/github-readme-stats)
- [GitHub Streak Stats](https://github.com/DenverCoder1/github-readme-streak-stats)
- [GitHub Profile Trophy](https://github.com/ryo-ma/github-profile-trophy)
- [Snake Animation](https://github.com/Platane/snk)
- [WakaTime Stats](https://github.com/anmol098/waka-readme-stats)

---

⭐ これらのツールを使用して、より魅力的な GitHub プロフィールページを作成しましょう！
