# Artisanの基本設定ガイド

参考URL
https://www.youtube.com/watch?v=S8LPIbF9Rx4

かなりしっかり設定している
https://www.youtube.com/watch?v=AB6nMEaEIZU

## 1. グラフの軸設定
### 温度軸（左軸）の設定
- メニュー → 構成 → グラフパーツを選択
- 温度軸の設定
  - 最小値：70度（推奨）
  - 最大値：230度（推奨）
  - 理由：レンジを狭くすることでグラフの傾きが大きくなり、温度変化が見やすくなる
  - ステップ：50度単位で表示

### RoR軸（右軸）の設定
- デルタ軸の設定
  - 最小値：0
  - 最大値：20
  - ステップ：5度単位で表示

### 時間軸（横軸）の設定
- オート設定推奨
- 焙煎時間に応じて自動調整される

## 2. ガス圧・排気ボタンの設定
### ボタンの作成手順
1. メニュー → 構成 → イベント → ボタンを選択
2. 「追加」ボタンで新規作成
3. 設定項目：
   - ラベル：ボタン上の表示文字
   - 記述：ボタンを押したときの表示文字
   - タイプ：
     - 排気の場合：空気
     - ガス圧の場合：バーナー
   - 値：グラフ上の表示位置（温度軸の値）

## 3. RoRの表示設定
### 表示項目の選択
1. メニュー → 構成 → 曲線を選択
2. 以下の項目にチェックを入れる：
   - BT（豆温度）のRoR
   - ET（排気温度）のRoR

## 4. フェーズカラーの設定
### 色の設定方法
1. メニュー → 構成 → カラーを選択
2. グラフメニューで各フェーズの色を設定：
   - ドライングフェーズ
   - メイラードフェーズ
   - フィニッシングフェーズ

## 5. フェーズ温度の設定
1. メニュー → 構成 → フェーズを選択
2. 各フェーズの開始温度を設定：
   - メイラードフェーズ：例）150度
   - デベロップメントフェーズ：例）190度

## 6. バックグラウンドプロファイルの表示
1. メニュー → 焙煎 → プロファイルの背景を選択
2. ロードから過去のプロファイルを選択

## 7. フィルターとスムージングの設定
### 基本設定
1. メニュー → 構成 → カーブ → フィルターを選択
2. 設定項目：
   - インプットフィルター：
     - ドロップスパイク：急激な温度低下のフィルタリング
     - リミット：上限・下限値の設定
   - カーブフィルター：スムージングの強度設定

### RoRフィルター設定
- デルタスパン：
  - 推奨値：1-10秒
  - 注意：大きすぎる値は応答遅延の原因となる
- スムージング：
  - BT（豆温度）とET（排気温度）それぞれに設定
  - 適度な値を設定し、データの精度と見やすさのバランスを取る

## 8. 設定の保存
1. メニュー → ヘルプ → セーブセッティング
2. 次回起動時：ロードセッティングから保存したデータを読み込み可能
   - 通常は最後の設定が自動的に読み込まれる 