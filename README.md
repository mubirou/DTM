# DTM

### <b>INDEX</b>
* [ドラムセット](#DrumSet): GM音源のドラムセットを利用する
* [レイテンシー](#Latency): ASIO4ALLを使ってレイテンシーを小さくする
* [クオンタイズ](#AutoQuantize): クオンタイズをグリッドに揃える
* [ベロシティ](#AutoVelocity): ベロシティをベタで揃える
* [ドラムパターン](#DrumPattern): 作曲に使える主なドラムパターン
* [コード進行](#ChordProgression): 作曲に使える主なコード進行
* [GrageBand](https://github.com/mubirou/DTM/tree/main/garageband): Apple GarageBandのサンプル（旧）

***


<a name="DrumSet"></a>
## ドラムセット

### 説明
GM（General MIDI）の「チャンネル10番」にはドラムセットなどパーカッション用（リズム音色）が予約されています。ここではドラムセットに含まれる主な音色をピックアップします。

### 使い方
1. "Insert MIDI Track"（MIDIトラックの挿入）
1. "Enable Inline MIDI Editing"（インラインMIDI編集を有効にする）
1. "MIDI Output"（MIDI出力）を"DLS Soft Synth"（DLSソフトシンセ）に設定
1. "MIDI Channel"（MIDIチャンネル）を"10"に設定
1. "Drum Kits"（ドラムキット）は"Standard"に設定

|通称|音階|音色名|概要|nanoKEY2|
|:--:|:--:|:--|:--|:--:|
|バスドラ|C|Bass Drum 1|大ダイコ（フットペダルで叩く）|-1 OCT|
|スネア|D|Acoustic Snare|小ダイコ|-1 OCT|
|ハイハット①|F#|Closed Hi-hat|2枚のシンバル（フットペダルで開閉）|-1 OCT|
|フロア|G|High Floor Tom|床に置くタムタム|-1 OCT|
|タムタム②|A|Low Tom|（使わない）|-1 OCT|
|ハイハット②|A#|Open Hi-hat|2枚のシンバル（フットペダルで開閉）|-1 OCT|
|タムタム①|D2|High Tom|リズムの切れ目に入れる|-1 OCT|
|クラッシュシンバル|C#2|Crash Cymbal 1|アクセント用（両サイドの小シンバル）|-1 OCT|
|ライドシンバル|D#2|Ride Cymbal 1|基本リズムを刻む（大きめのシンバル）|-1 OCT|

実行環境：ACID Xpress 7、ACID Pro 10、KORG nanoKEY2   
作成者：夢寐郎  
作成日：2020年10月21日  


<a name="Latency"></a>
## レイテンシー

### 説明
レイテンシーを小さくするためにASIOドライバ（ASIO4ALL）を使います。MIDIキーボード入力の遅れがなくなります。


### 設定方法
1. http://www.asio4all.org/ から「ASIO4ALL 2.14」をインストール
1. ACIDの[オプション]-[ユーザー設定]-[オーディオデバイス]の「オーディオデバイスの種類」から「ASIO4ALL v2」を選択し「適用」  
（Xpressの場合[Options]-[Preferences]-[Audio Device]-[Audio device]-[ASIO4ALL v2]）
1. 引き続き「詳細」（Advanced）を選択
1. 「オーディオの詳細設定」の「設定」（Configure）を選択
1. 「ASIO4ALL v2.14」設定画面で、利用したいオーディオインターフェイス（AKG C44-USB Microphone）を選択
1. Windowsの[設定]-[システム]-[サウンド]-[出力デバイスを選択してください]で上記のオーディオインターフェイスを選択

実行環境：ACID Pro 10、ACID Xpress 7、AKG Lyra、ASIO4ALL v.2.14  
作成者：夢寐郎  
作成日：2020年10月22日  
更新日：2020年10月24日


<a name="AutoQuantize"></a>
## クオンタイズ

### 説明
MIDIキーボードを使ってリアルタイムレコーディングしたものを、16分音符のグリッドにかっちり揃えます。

### 操作方法
1. グリッドに揃えたいMIDIトラックを選択。
1. [編集]-[MIDIプロセスとフィルタ]-[クオンタイズ]を選択。
1. 次の項目を選択して「適用」を押す。
    * クオンタイズスタート
    * クオンタイズリリース
    * 選択したトラックのすべての音符に適用

実行環境：ACID Pro 10、ACID Xpress 7  
作成者：夢寐郎  
作成日：2020年10月22日  


<a name="AutoVelocity"></a>
## ベロシティ

### 説明
MIDIキーボードを使ってリアルタイムレコーディングしたもののベロシティをベタで揃えます。

### 操作方法
1. ベロシティを揃えたいMIDIトラックを選択。  
    ベロシティが表示されていない場合、[表示]-[インラインMIDI編集の表示]-[ノートオンベロシティ]で表示。
1. [編集]-[MIDIプロセスとフィルタ]-[ベロシティ]を選択。  
 （Xpressの場合は[Edit]-[MIDI Processes Filters]-[Velocity]）
1. 次の項目を選択または設定して「適用」を押す。
    * スタート ベロシティ（Change Start Velocity）：✔
    * リリース ベロシティ（Change Release Velocity）：✔
    * 値の設定: 100（1～127／初期値64）
    * 選択したトラックのすべての音符に適用（Apply to all notes selected tracks）

実行環境：ACID Pro 10、ACID Xpress 7  
作成者：夢寐郎  
作成日：2020年10月22日  
更新日：2020年10月24日


<a name="DrumPattern"></a>
## ドラムパターン

|No.|種類|概要|.mid|.mp3|備考|
|:--:|:--|:--|:--:|:--:|:--|
|1|8ビート|8分音符主体（Hi-hat版）ROCK･POPS|[●](https://mubirou.github.io/DTM/mid/drum01_8beat_Hi-hat.mid)|[●](https://mubirou.github.io/DTM/mp3/drum01_8beat_Hi-hat.mp3)||
|2|8ビート|同上（Ride Cymbal版）|[●](https://mubirou.github.io/DTM/mid/drum02_8beat_RideCymbal.mid)|[●](https://mubirou.github.io/DTM/mp3/drum02_8beat_RideCymbal.mp3)||
|3|8ビート|同上（Floor Tom版）|[●](https://mubirou.github.io/DTM/mid/drum03_8beat_FloorTom.mid)|[●](https://mubirou.github.io/DTM/mp3/drum03_8beat_FloorTom.mp3)||
|4|16ビート|16分音符主体, FUNK･ROCK･J-POP|[●](https://mubirou.github.io/DTM/mid/drum04_16beat.mid)|[●](https://mubirou.github.io/DTM/mp3/drum04_16beat.mp3)||
|5|シャッフルビート|Swing, 8ビートのシャッフル版|[●](https://mubirou.github.io/DTM/mid/drum05_shuffle_8beat.mid)|[●](https://mubirou.github.io/DTM/mp3/drum05_shuffle_8beat.mp3)||
|6|シャッフルビート|Swing, 16ビートのシャッフル版|[●](https://mubirou.github.io/DTM/mid/drum06_shuffle_16beat.mid)|[●](https://mubirou.github.io/DTM/mp3/drum06_shuffle_16beat.mp3)|※1|
|7|シェイクビート|8ビート+16分裏にスネア|[●](https://mubirou.github.io/DTM/mid/drum07_shake_8beat.mid)|[●](https://mubirou.github.io/DTM/mp3/drum07_shake_8beat.mp3)||


※1 16ビートのシャッフル化は [編集]-[MIDIプロセスとフィルタ]-[クオンタイズ] で [16分音符][連符(3/2)] を適用することで可能。

* 参考：https://www.youtube.com/watch?v=_YgCsGy_rHA

実行環境：ACID Pro 10   
作成者：夢寐郎  
作成日：2020年10月24日  
更新日：2020年11月09日  


<a name="ChordProgression"></a>
## コード進行

|No.|進行名|コード進行|.mid|.mp3|備考|
|:--:|:--|:--|:--:|:--:|:--|
|1|王道進行|F-G-Em-Am|[●](https://mubirou.github.io/DTM/mid/chord01_oudou.mid)|[●](https://mubirou.github.io/DTM/mp3/chord01_oudou.mp3)||
|2|椎名林檎進行|FM7-E7-Am7-CM7|[●](https://mubirou.github.io/DTM/mid/chord02_shiina.mid)|[●](https://mubirou.github.io/DTM/mp3/chord02_shiina.mp3)||
|3|4156進行|F-C-G-Am|[●](https://mubirou.github.io/DTM/mid/chord03_4156.mid)|[●](https://mubirou.github.io/DTM/mp3/chord03_4156.mp3)|次世代の王道進行|
|4|カノン進行|C-G-Am-Em-F-C-F-G|[●](https://mubirou.github.io/DTM/mid/chord04_canon.mid)|[●](https://mubirou.github.io/DTM/mp3/chord04_canon.mp3)||
|5|小室進行|Am-F-G-C|[●](https://mubirou.github.io/DTM/mid/chord05_komuro.mid)|[●](https://mubirou.github.io/DTM/mp3/chord05_komuro.mp3)||
|6|Let It Be進行|C-G-Am-F|[●](https://mubirou.github.io/DTM/mid/chord06_letItBe.mid)|[●](https://mubirou.github.io/DTM/mp3/chord06_letItBe.mp3)||

* 参考：https://www.youtube.com/watch?v=tE-b4nvusB8

実行環境：ACID Pro 10  
作成者：夢寐郎  
作成日：2020年10月31日  
更新日：2020年11月09日