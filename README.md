# 抽選アプリ

シンプルで使いやすい抽選アプリです。3つのPOT(赤・青・緑)から順番に人物名を表示します。

## 🚀 デモ

GitHub Pagesでホスティング後、以下のURLでアクセスできます:
```
https://your-username.github.io/your-repository-name/
```

## 📋 機能

- **3つのPOT**: POT1(赤)、POT2(青)、POT3(緑)に分けて人物名を管理
- **順番表示**: 登録順に1名ずつ表示(ランダムではありません)
- **残数表示**: 各POTの残り人数をリアルタイム表示
- **自動無効化**: 全員が選ばれたらボタンがグレーアウト
- **抽選履歴**: いつ誰が選ばれたか記録
- **GitHub連携**: data.jsonファイルで簡単にデータ管理

## 🛠️ セットアップ

### 1. GitHubリポジトリの作成

```bash
# 新しいリポジトリを作成してクローン
git clone https://github.com/your-username/your-repository-name.git
cd your-repository-name

# ファイルを配置
# - index.html (メインアプリ)
# - data.json (人物名データ)
# - README.md (このファイル)
```

### 2. GitHub Pagesを有効化

1. GitHubのリポジトリページを開く
2. Settings > Pages に移動
3. Source を **main** ブランチの **/ (root)** に設定
4. Save をクリック
5. 数分後、`https://your-username.github.io/your-repository-name/` でアクセス可能に

## 📱 使い方

### PCでの準備(人物名の登録・更新)

1. ブラウザで `index.html` を開く
2. 各POTに人物名を入力(1行1名)
3. **「📥 data.json をダウンロード」**ボタンをクリック
4. ダウンロードした `data.json` をリポジトリに配置
5. Gitでプッシュ

```bash
git add data.json
git commit -m "Update lottery data"
git push
```

### スマホでの抽選

1. GitHub PagesのURLにアクセス
   - `https://your-username.github.io/your-repository-name/`
2. 自動的に最新の `data.json` が読み込まれます
3. 「抽選を開始」をタップ
4. 各POTの「抽選」ボタンをタップして順番に表示

## 📄 data.json のフォーマット

```json
{
  "version": "1.0",
  "lastUpdated": "2025-12-04T00:00:00.000Z",
  "pots": {
    "1": [
      "山田太郎",
      "鈴木花子",
      "佐藤次郎"
    ],
    "2": [
      "田中一郎",
      "高橋美咲",
      "伊藤健太"
    ],
    "3": [
      "渡辺さくら",
      "中村大輔",
      "小林愛"
    ]
  }
}
```

## 🔄 データ更新のワークフロー

```
PC側:
1. index.html を開く
2. 人物名を編集
3. data.json をダウンロード
4. git push

スマホ側:
1. GitHub Pages URL にアクセス
2. ページをリロード(最新データが読み込まれる)
3. 抽選開始
```

## 💡 Tips

### キャッシュのクリア
もしスマホで最新データが反映されない場合:
- ブラウザのキャッシュをクリア
- または、アプリ内の「🔄 data.json を再読み込み」ボタンをタップ

### 直接編集
GitHubのWebエディタで `data.json` を直接編集することも可能です:
1. GitHubで `data.json` を開く
2. 鉛筆アイコン(編集)をクリック
3. 編集して Commit changes

### ローカルでの使用
GitHub Pages を使わず、ローカルで使用する場合:
- `index.html` と `data.json` を同じフォルダに配置
- `index.html` をブラウザで開く

## 🎨 カスタマイズ

### 色の変更
`index.html` の `<style>` セクションで色をカスタマイズできます:
```css
.pot-card.pot1 { border-top: 5px solid #e74c3c; } /* POT1の色 */
.pot-card.pot2 { border-top: 5px solid #3498db; } /* POT2の色 */
.pot-card.pot3 { border-top: 5px solid #2ecc71; } /* POT3の色 */
```

### POTの絵文字変更
`index.html` の該当箇所を編集:
```html
<div class="pot-image">🏺</div> <!-- 好きな絵文字に変更 -->
```

## 📝 ライセンス

MIT License - 自由に使用・改変できます

## 🤝 サポート

問題や質問がある場合は、GitHubのIssuesで報告してください。
