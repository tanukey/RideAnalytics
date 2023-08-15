# RideAnalytics
## 概要
Garminなどで記録できる.fitファイルからその日の練習内容を可視化・振り返るためのサンプルコード

## 各関数について
### return_ridedata
- 入力：.fitファイルを指定する。
- 出力：後述の各関数で指定するためのride_dataを返却する。
### plot_map
- 入力：ride_data
- 出力：GPS情報からOpenStreetMap地図にプロットした地図データを返却する。
### plot_ride_summary
- 入力：ride_data,smoothness_window:int 数値を平均化する秒数を指定する。
- 出力：時間をx軸に、パワー、ケイデンス、スピード、標高をプロットした線グラフ
### plot_watt_torque_summary
- 入力：ride_data,smoothness_window:int 数値を平均化する秒数を指定する。ftp:int 自分のFTPを指定する。
- 出力：時間をx軸に、パワー、トルクをプロットした線グラフ
### calc_trainning_indicator
- 入力：ride_data,ftp:int 自分のFTPを指定する。
- 出力：NormalizedPower,IntensityFactor,TrainningStressSoreを計算した辞書
### plot_power_zone
- 入力：ride_data,ftp:int 自分のFTPを指定する。
- 出力：L1〜7各ゾーンの滞在時間をプロットした棒グラフ
### plot_watt_torque_curve
- 入力：ride_data
- 出力：出力とトルクの各時間最大値をプロットした線グラフ