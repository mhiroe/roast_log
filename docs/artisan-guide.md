# Artisan ロースト記録ガイド

## 概要

Artisanは、コーヒーロースティングのプロセスを記録、分析、制御するための高度なソフトウェアです。このガイドでは、主要な機能とパラメータについて説明します。

## 基本設定

### 表示モード
- `mode`: 温度表示モード
  - 'C': 摂氏温度（デフォルト）
  - 'F': 華氏温度
- `viewerMode`: ビューワーモードの設定
  - `true`: 読み取り専用モード
  - `false`: 編集可能モード

### グラフ表示設定
- `graphstyle`: グラフの表示スタイル
- `graphfont`: 使用するフォント
- `title_show_always`: タイトルの常時表示設定
- `zoom_follow`: ズーム時の追従設定

## カラーパレット

### 基本カラー
```json
{
    "background": "#ffffff",    // 背景色
    "grid": "#e5e5e5",         // グリッド線
    "ylabel": "#808080",       // Y軸ラベル
    "xlabel": "#808080",       // X軸ラベル
    "title": "#0c6aa6",        // タイトル
    "canvas": "#f8f8f8"        // キャンバス背景
}
```

### 温度曲線カラー
```json
{
    "et": "#cc0f50",          // 環境温度線
    "bt": "#0a5c90",          // 豆温度線
    "deltaet": "#cc0f50",     // ET変化率
    "deltabt": "#0a5c90"      // BT変化率
}
```

## フレーバー評価システム

### 標準フレーバー評価項目
- Artisan標準:
  - Acidity（酸味）
  - Aftertaste（後味）
  - Clean Cup（クリーン度）
  - Head（ヘッド）
  - Fragrance（香り）
  - Sweetness（甘み）
  - Aroma（アロマ）
  - Balance（バランス）
  - Body（ボディ）

### SCAA評価項目
- Fragrance-Aroma（香り-アロマ）
- Flavor（フレーバー）
- Aftertaste（後味）
- Acidity（酸味）
- Body（ボディ）
- Uniformity（均一性）
- Balance（バランス）
- Clean Cup（クリーン度）
- Sweetness（甘み）
- Overall（総合評価）

## データ記録と分析

### 基本データ記録
- `samplinginterval`: サンプリング間隔（秒）
- `profile_sampling_interval`: プロファイル記録間隔
- `optimalSmoothing`: 最適化されたスムージング処理の有効/無効

### フィルタリング設定
- `filterDropOuts`: ドロップアウトフィルタリング
- `dropSpikes`: スパイクノイズの除去
- `dropDuplicates`: 重複データの除去
- `median_filter_factor`: メディアンフィルタの強度

### 自動記録設定
- `autosaveflag`: 自動保存の有効/無効
- `autosaveprefix`: 自動保存時のファイル名プレフィックス
- `autosavepath`: 自動保存先パス
- `autosaveimage`: 画像の自動保存

## イベント管理

### イベントタイプ
- `etypes`: イベントタイプの定義
  - 'Air': エアー制御イベント
  - 'Drum': ドラム制御イベント
  - 'Damper': ダンパー制御イベント
  - 'Burner': バーナー制御イベント
  - '--': その他のイベント

### イベント表示設定
- `eventsGraphflag`: イベントグラフの表示
- `clampEvents`: イベントの位置固定
- `renderEventsDescr`: イベント説明の表示
- `eventslabelschars`: イベントラベルの文字数制限
- `eventsshowflag`: イベント表示の有効/無効

## 注意事項

1. 温度データは常に摂氏で内部保存され、表示時に必要に応じて華氏に変換されます
2. フレーバー評価は0-10のスケールで記録されます
3. イベントの時刻は常にUTCで保存され、表示時にローカルタイムに変換されます
4. 自動保存機能を使用する場合は、十分なディスク容量があることを確認してください
5. カスタムフレーバーラベルは設定ファイルに保存され、次回起動時に復元されます 