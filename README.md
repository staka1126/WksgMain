# Wakasagi_v1
これは、aruduinoを用いたワカサギ電動リールの制御ファームウェアおよび対応する回路図です。現在はESP32_Core_board_V2にしか対応していませんが、今後、機能を取捨選択しながらarduino nanoなどにも対応していくつもりです。また、外装は3Dプリンタで印刷できるようにSTLを公開する予定です。

## 機能概要
* 4つのボタン
  * 5段階の巻き上げ速度(S1)
  * カウンター機能(S2)
  * ちょい巻き機能(S3)
  * 船べり停止機能(S4)
* スマホ連携（BlueTooth/Wi-Fi接続）　★未実装
* OLED表示
* 設定値保存
* 外部電源
  
## 対応ボード
* ESP32_Core_board_V2
  
## 開発環境
* Arduino IDE v1.8.12
* Ubuntu 18.04.3 LTS / Windows10

## 機能詳細
### 4つのボタン
#### 5段階の巻き上げ速度(S1)
* 短押しで1速UP
* 長押し0.5sごとに1速ダウン
#### カウンター機能(S2)
* 短押しで1匹加算
* 長押し0.5sごとに1匹ずつ減算
* 減算10匹を超えると徐々に減らす速度が大きくなる
#### ちょい巻き機能(S3)
* 短押しで0.5sの巻き上げ
* 0.5s以上では、押し続けることでその間は巻き上げを継続
#### 船べり停止機能(S4)
* ビーズ等で巻き込みを防止することが可能
### スマホ連携（BlueTooth/Wi-Fi接続）　★未実装
* 日時（予定）
* 場所（予定）
* 釣果（予定）
* 1時間ごとの分析（予定）
* その他のログ機能（予定）
### OLED表示
* 釣り上げたワカサギの数の表示
* モーター速度表示
* モーター動作状態の表示
* 128x64のOLEDで見やすい
* 焼き付き防止のため、無操作5sで消灯します
### 設定値保存
* 電源が切れても、3分ごとに釣果を保存
* 次に起動したときは、前回のモーター速度を保持
### 外部電源
* 市販のモバイルバッテリーを接続して給電
  
## 回路図と部品リスト（電装系）
* Schematicフォルダ以下に電装系のBOMと回路図をおいています
* モーターや外装、リール、ネジ等は別途必要です
* モーターは3V以下で駆動するものを想定しています
  
## 3Dプリンタデータ
* 後日公開

## ライセンス
* GPL v3.0
