# UiFlow クイックスタート(Blockly/MicroPython)



?> **Note** *初めてM5Stackを使う場合、あらかじめ指定のファームウェアを書き込む必要があります。[ファームウェアの更新方法](ja/related_documents/how_to_burn_firmware)を参照してください。また、Wi-Fi接続先を変更したい場合は、このページを参照してください。 [M5StackのWi-Fi接続方法 (M5Cloud向け)](/ja/related_documents/how_to_connect_wifi_using_core_with_m5cloud)*

M5Stackを起動したらすぐに `UPLOAD` ボタンを連打します。以下の画面に遷移しなかった場合は、M5Stack本体横の赤いリセットスイッチを押して、再起動してやり直してください。

<figure>
    <img src="assets/img/getting_started_pics/m5stack_core/get_started_with_uiflow/apikey.jpg">
</figure>

?> **Note** *最初の起動では何もしないと、デモプログラムに遷移します。Wi-Fiの設定が完了していると自動的にWi-FiのAPに接続しにいきます。Wi-Fiを再設定したい場合は、`SETUP`ボタンを押してください。*

## コンテンツ

1. [UiFlowに接続](#_1-uiflowに接続)

2. [プログラム作成](#_2-プログラム作成)

3. [音楽演奏デモ](#_3-音楽演奏デモ)

## 1. UiFlowに接続

1. M5Stackに表示されている二次元コードをあなたのスマートフォンやタブレットPCで読み取ってプログラムを始めることができます。もしPCでプログラムをする場合は、ブラウザで次のURLを入力してください。 `flow.m5stack.com`

<figure>
    <img src="assets/img/getting_started_pics/m5stack_core/get_started_with_uiflow/webide.png">
</figure>

1. UiFlowを利用するためには、お持ちのM5Stackをペアリングする必要があります。

最初にUiFlowの画面の右上にある歯車の設定を開きます。`APIKEY` の欄にM5Stack本体に表示されているAPIKEYを入力します。(写真の場合は `9C6469`) 入力が終わったら`SAVE`をクリックします。

<figure>
    <img src="assets/img/getting_started_pics/m5stack_core/get_started_with_uiflow/click_for_apikey.png">
</figure>

<figure>
    <img src="assets/img/getting_started_pics/m5stack_core/get_started_with_uiflow/input_apikey.png">
</figure>

正しいAPIKEYが入力されるとUiFlowはあなたのM5Stackと接続します。

しばらくすると下図のように、Blockly(や Python)を用いてプログラムが可能になります。

## 2. プログラム作成

### a. UIデザイン

4種類のUI要素が用意されており、UiFlow内のUIエディタにドラッグすることで利用できます。試しにいくつかUIオブジェクトを配置して`実行(Run)`をクリックしてみましょう。

<figure>
    <img src="assets/img/getting_started_pics/m5stack_core/get_started_with_uiflow/draw_ui.png">
</figure>

<figure>
    <img src="assets/img/getting_started_pics/m5stack_core/get_started_with_uiflow/run_and_upload.png">
</figure>

### b. Blocklyでプログラミング

`Emoji`クラスの中にある`Set emoji map in0`ブロックをドラッグしてブロックエディタに配置し、`実行(Run)`をクリックしてみましょう。

<figure>
    <img src="assets/img/getting_started_pics/m5stack_core/get_started_with_uiflow/draw_heart.png">
</figure>

<figure>
    <img src="assets/img/getting_started_pics/m5stack_core/get_started_with_uiflow/run_and_upload.png">
</figure>

### c. MicroPythonでプログラミング

Blockly/MicroPython切り替えボタンを使って、MicroPythonに切り替えます。そして次のコードをコピーして`Python エディタ`に貼り付け、`実行(Run)`をクリックしてみましょう。

```Python
from m5stack import *
from m5ui import *
clear_bg(0x111111)


btnA = M5Button(name='ButtonA', text='ButtonA', visibility=False)
btnB = M5Button(name='ButtonB', text='ButtonB', visibility=False)
btnC = M5Button(name='ButtonC', text='ButtonC', visibility=False)


lcd.print("Hello M5Stack")
```

<figure>
    <img src="assets/img/getting_started_pics/m5stack_core/get_started_with_uiflow/program_with_micropython.png">
</figure>

M5Stackの画面に`Hello M5Stack`と表示されます。

## 3. 音楽演奏デモ

M5Stackを用いればたった数分でミュージックプレイヤーを作成して、音楽を演奏することができます。

`loop`、`music`、`timer`から下図のブロックをブロックエディタに配置します。

<figure>
    <img src="assets/img/getting_started_pics/m5stack_core/get_started_with_uiflow/drag_loop_block.png">
</figure>

<figure>
    <img src="assets/img/getting_started_pics/m5stack_core/get_started_with_uiflow/drag_music_block.png">
</figure>

<figure>
    <img src="assets/img/getting_started_pics/m5stack_core/get_started_with_uiflow/drag_timer_block.png">
</figure>

それから下図に示すように各ブロックのパラメータを調整します。

<figure>
    <img src="assets/img/getting_started_pics/m5stack_core/get_started_with_uiflow/whole_program.png">
</figure>

完成したら、鳴らしてみましょう！！

## 完成

?> **Note** *M5StackへのWorkShop等のお問い合わせはこちらまで→ <support@m5stack.com>*
