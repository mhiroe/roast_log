# 温度とイベント

## 温度データ

### 基本温度データ
- `temp1`: ET（環境温度）データ配列
- `temp2`: BT（豆温度）データ配列
- `timex`: 時間データ配列（秒）

### 環境データ
- `ambientTemp`: 周辺温度
- `ambient_humidity`: 周辺湿度
- `ambient_pressure`: 大気圧
- `moisture_greens`: 生豆の水分量
- `greens_temp`: 生豆の温度
- `moisture_roasted`: 焙煎後の水分量

## イベントデータ

### 特殊イベント
- `specialevents`: イベントのタイムスタンプ配列
- `specialeventstype`: イベントタイプ配列
- `specialeventsvalue`: イベント値配列
- `specialeventsStrings`: イベント説明文字列配列

### イベントタイプ
- `etypes`: イベントタイプ定義
  - 'Air': エアー制御
  - 'Drum': ドラム制御
  - 'Damper': ダンパー制御
  - 'Burner': バーナー制御
  - '--': その他

### フェーズマーカー
- `phases`: ロースティングフェーズの区切り位置
  - ドライフェーズ開始
  - ミドルフェーズ開始
  - フィニッシュフェーズ開始
  - クーリング開始

## 計算値

### 基本計算値
- `computed.CHARGE_ET`: 投入時のET温度
- `computed.CHARGE_BT`: 投入時のBT温度
- `computed.TP_idx`: ターニングポイントのインデックス
- `computed.TP_time`: ターニングポイントまでの時間
- `computed.TP_ET`: ターニングポイント時のET温度
- `computed.TP_BT`: ターニングポイント時のBT温度
- `computed.MET`: 最高ET温度

### フェーズ時間
- `computed.DRY_time`: ドライフェーズの時間
- `computed.DRY_ET`: ドライフェーズ終了時のET
- `computed.DRY_BT`: ドライフェーズ終了時のBT
- `computed.FCs_time`: ファーストクラック開始時間
- `computed.FCs_ET`: ファーストクラック開始時のET
- `computed.FCs_BT`: ファーストクラック開始時のBT
- `computed.DROP_time`: ドロップ時間
- `computed.DROP_ET`: ドロップ時のET
- `computed.DROP_BT`: ドロップ時のBT

### フェーズ分析
- `computed.dryphasetime`: ドライフェーズの長さ
- `computed.midphasetime`: ミドルフェーズの長さ
- `computed.finishphasetime`: フィニッシュフェーズの長さ
- `computed.totaltime`: 総ロースト時間

### レート分析
- `computed.dry_phase_ror`: ドライフェーズの昇温率
- `computed.mid_phase_ror`: ミドルフェーズの昇温率
- `computed.finish_phase_ror`: フィニッシュフェーズの昇温率
- `computed.total_ror`: 全体の平均昇温率
- `computed.fcs_ror`: ファーストクラック時の昇温率

### 温度差分析
- `computed.dry_phase_delta_temp`: ドライフェーズの温度変化
- `computed.mid_phase_delta_temp`: ミドルフェーズの温度変化
- `computed.finish_phase_delta_temp`: フィニッシュフェーズの温度変化 