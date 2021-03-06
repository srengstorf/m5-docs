# NeoPixel ユニット

<img src="assets/img/product_pics/unit/M5GO_Unit_neopixel.png" width="30%" height="30%">

***

:memo:**[概要](#概要)**&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;:octocat:**[サンプルコード](#サンプルコード)**&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;🛒**[購入リンク](https://www.aliexpress.com/store/product/M5Stack-Official-NeoPixel-RGB-LEDs-Cable-SK6812-with-GROVE-Port-2m-1m-50cm-20cm-10cm/3226069_32950831315.html?spm=a2g1x.12024536.productList_5885013.pic_0)**&nbsp;&nbsp;&nbsp;:clapper:**[関連動画](#関連動画)**

## 概要

**<mark>NeoPixel</mark>**ユニットは帯状にフルカラーLEDが連なったケーブルです。プログラマブルに色や点灯・点滅などをコントロールする事が可能です。Grove インターフェースで接続します。

?> NeoPixel Unit入力ポートと出力ポートがあります。

<img src="assets/img/product_pics/unit/unit_neopixel_02.png">

## 特徴

- 測定可能距離: 10cm/20cm/0.5m/1m/2m
- Grove インターフェース
- LEGO 互換ホール

## サンプルコード

### 1. Arduino IDE

*特定のルーチンが必要な場合はここをクリックしてください[ルーチン](https://github.com/m5stack/M5-ProductExampleCodes/tree/master/Unit/NEOPIXEL/Arduino)。*

```arduino
/*
    Install FastLED library first.
*/
#include <M5Stack.h>
#include "FastLED.h"

#define Neopixel_PIN    21
#define NUM_LEDS    30

CRGB leds[NUM_LEDS];
uint8_t gHue = 0;
static TaskHandle_t FastLEDshowTaskHandle = 0;
static TaskHandle_t userTaskHandle = 0;

void setup(){
  Serial.begin(115200);
  M5.begin();
  M5.Lcd.clear(BLACK);
  M5.Lcd.setTextColor(YELLOW); M5.Lcd.setTextSize(2); M5.Lcd.setCursor(40, 0);
  M5.Lcd.println("Neopixel example");
  M5.Lcd.setTextColor(WHITE);
  M5.Lcd.setCursor(0, 25);
  M5.Lcd.println("Display rainbow effect");

  // Neopixel initialization
  FastLED.addLeds<WS2811,Neopixel_PIN,GRB>\
                         (leds, NUM_LEDS).setCorrection(TypicalLEDStrip);
  FastLED.setBrightness(10);
  xTaskCreatePinnedToCore(FastLEDshowTask, \
                         "FastLEDshowTask", 2048, NULL, 2, NULL, 1);
}

void loop(){
}

void FastLEDshowESP32(){
    if (userTaskHandle == 0){
        userTaskHandle = xTaskGetCurrentTaskHandle();
        xTaskNotifyGive(FastLEDshowTaskHandle);
        const TickType_t xMaxBlockTime = pdMS_TO_TICKS( 200 );
        ulTaskNotifyTake(pdTRUE, xMaxBlockTime);
        userTaskHandle = 0;
    }
}

void FastLEDshowTask(void *pvParameters){
    for(;;){
        fill_rainbow(leds, NUM_LEDS, gHue, 7);// rainbow effect
        FastLED.show();// must be executed for neopixel becoming effective
        EVERY_N_MILLISECONDS( 20 ) { gHue++; }
    }
}
```

<img src="assets/img/product_pics/unit/unit_example/NEOPIXEL/example_unit_neopixel_02.png">

### 2. UIFlow

*特定のルーチンが必要な場合はここをクリックしてください[ルーチン](https://github.com/m5stack/M5-ProductExampleCodes/tree/master/Unit/NEOPIXEL/UIFlow)。*

<img src="assets/img/product_pics/unit/unit_example/NEOPIXEL/example_unit_neopixel_01.png">

### ピンマップ

<table>
 <tr><td>M5Core(GROVEインターフェースA)</td><td>GPIO22</td><td>GPIO21</td><td>5V</td><td>GND</td></tr>
 <tr><td>NEOPIXEL Unit</td><td> </td><td>デジタルピン</td><td>5V</td><td>GND</td></tr>
</table>

## 関連リンク

- **[公式ビデオ](https://www.youtube.com/channel/UCozgFVglWYQXbvTmGyS739w)**

- **[フォーラム](http://forum.m5stack.com/)**

- **[FastLED図書館](https://github.com/FastLED/FastLED/wiki/Overview)**

- **[FastLED参照(中国語)](http://www.taichi-maker.com/homepage/reference-index/arduino-library-index/fastled-library/)**

## 関連動画

**Neopixel**

<iframe height=498 width=510 src='https://player.youku.com/embed/XMzg3NzE3NzY0MA==' frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>