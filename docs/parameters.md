# Artisan パラメータ

## 基本パラメータ

### バージョン情報
- `version`: Artisanのバージョン番号
- `revision`: リビジョン番号
- `build`: ビルド番号
- `artisan_os`: 実行OSの種類
- `artisan_os_version`: 実行OSのバージョン
- `artisan_os_arch`: 実行OSのアーキテクチャ

### ロースト情報
- `mode`: ロースティングモード（'C'=摂氏、'F'=華氏）
- `viewerMode`: ビューワーモードの有効/無効
- `timeindex`: タイムインデックス配列
- `title`: ロースト名
- `locale`: 使用言語設定
- `roastdate`: ロースト日付
- `roasttime`: ロースト時刻
- `roastepoch`: ロースト開始時のUNIXタイムスタンプ
- `roasttzoffset`: タイムゾーンオフセット（秒）

### 豆情報
- `beans`: 豆の名前
- `weight`: 重量 [値, 単位, 'g']
- `volume`: 容量 [値, 単位, 'l']
- `density`: 生豆密度 [値, 'g', 1, 'l']
- `density_roasted`: 焙煎後の密度 [値, 'g', 1, 'l']
- `beansize`: 豆のサイズ
- `beansize_min`: 最小豆サイズ
- `beansize_max`: 最大豆サイズ

### ロースター情報
- `roastertype`: ロースターの種類
- `roastersize`: ロースターのサイズ
- `roasterheating`: ヒーティング方式
- `machinesetup`: マシン設定
- `operator`: オペレーター名
- `organization`: 組織名
- `drumspeed`: ドラム回転速度

## フレーバープロファイル

### フレーバー評価
- `flavors`: フレーバースコア配列
- `flavorlabels`: フレーバーラベル配列
  - 'Acidity' (酸味)
  - 'Aftertaste' (後味)
  - 'Clean Cup' (クリーン度)
  - 'Head' (ヘッド)
  - 'Fragrance' (香り)
  - 'Sweetness' (甘み)
  - 'Aroma' (アロマ)
  - 'Balance' (バランス)
  - 'Body' (ボディ)
- `flavorstartangle`: フレーバーホイールの開始角度
- `flavoraspect`: フレーバーホイールのアスペクト比

## 品質評価パラメータ

### 欠点評価
- `heavyFC`: 重度のファーストクラック
- `lowFC`: 弱いファーストクラック
- `lightCut`: ライトカット
- `darkCut`: ダークカット
- `drops`: ドロップ
- `oily`: オイリー
- `uneven`: 不均一
- `tipping`: ティッピング
- `scorching`: スコーチング
- `divots`: ディボット

### 色評価
- `whole_color`: 全体の色
- `ground_color`: 挽いた後の色
- `color_system`: 使用する色評価システム 