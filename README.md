# DTM
音楽的あるいは技術的な裏付けは皆無の作曲･編曲




### <b>INDEX</b>
* [ASIO4ALL](#ASIO4ALL): ASIOドライバを利用してレイテンシーを小さくする
* [GMチャンネル10番](#GMChannel10): パーカッション
* [XXXXX](#XXXXX): XXXXXXX
* [XXXXX](#XXXXX): XXXXXXX
* [XXXXX](#XXXXX): XXXXXXX
* [XXXXX](#XXXXX): XXXXXXX
* [XXXXX](#XXXXX): XXXXXXX
* [XXXXX](#XXXXX): XXXXXXX
* [XXXXX](#XXXXX): XXXXXXX
* [XXXXX](#XXXXX): XXXXXXX
* [XXXXX](#XXXXX): XXXXXXX

***

<a name="ASIO4ALL"></a>
# ASIO4ALL

### 説明
レイテンシーを小さくするためにASIOドライバ（ASIO4ALL）を使います


### 設定方法
1. http://www.asio4all.org/ から「ASIO4ALL 2.14」をインストール
1. ACIDの[オプション]-[ユーザー設定]-[オーディオデバイス]の「オーディオデバイスの種類」から「ASIO4ALL v2」を選択し「適用」
1. 引き続き「詳細」を選択
1. 「オーディオの詳細設定」の「設定」を選択
1. 「ASIO4ALL v2.14」設定画面で、利用したいオーディオインターフェイス（AKG C44-USB Microphone）を選択  

実行環境：ACID Pro 10、ACID Xpress 7、AKG Lyra、KORG nanoKEY2、ASIO4ALL v.2.14  
作成者：夢寐郎  
作成日：2020年10月22日  


<a name="GMChannel10"></a>
# GMチャンネル10番

### 説明
GM（General MIDI）のチャンネル10番に、ドラムセットなどパーカッション用（リズム音色）が予約されている。

### 使い方
1. 「MIDIトラックの挿入」
1. 「インラインMIDI編集を有効にする」
1. MIDI出力を「DLSソフトシンセ」に設定（重要）
1. MIDIチャンネルを「10」に設定（重要）
1. ドラムキットは「Standard」に設定

|nanoKEY2|音階|name|概要|
|:--:|:--|:--|:--:|
|-1 OCT|C|バス ドラム1|大ダイコ|
|-1 OCT|D|アコースティック スネア|小ダイコ|
|-1 OCT|F#|クローズド ハイハット|2枚のシンバル|
|-1 OCT|G|ハイ フロアタム|XXXX|
|-1 OCT|A#|オープンハイハット|2枚のシンバル|
|-1 OCT|D2|ハイタム|XXXX|
|-1 OCT|C#2|クラッシュシンバル1|アクセント用|
|-1 OCT|D#2|ライド シンバル1|基本リズムを刻む|

実行環境：ACID Pro 10、ACID Xpress 7、KORG nanoKEY2   
作成者：夢寐郎  
作成日：2020年10月2X日  