# 灰色升级版M5Core

<img src="assets/img/product_pics/core/gray/gray_01.png" alt="gray_02" width="250" height="250"> <img src="assets/img/product_pics/core/gray/gray_02.png" alt="gray_02" width="250" height="250"> <img src="assets/img/product_pics/core/gray/gray_04.png" alt="gray_04" width="65%" height="65%">

<!-- <img src="assets/img/product_pics/core/gray/gray_03.png" alt="gray_03" width="250" height="250"> -->

* * *

:memo:**[Description](#Description)**&nbsp;&nbsp;&nbsp;:bulb:**[Quick Start](en/quick_start/m5core/m5stack_core_quick_start)**&nbsp;&nbsp;&nbsp;:octocat:**[Example](https://github.com/m5stack/M5Stack/tree/master/examples/Basics)**&nbsp;&nbsp;&nbsp;:electric_plug:**[Schematic](https://github.com/m5stack/M5-Schematic/blob/master/Core/Basic/M5-Core-Schematic(20171206).pdf)**&nbsp;&nbsp;&nbsp;🛒**[Purchase](https://www.aliexpress.com/store/product/M5Stack-Official-In-Stock-ESP32-Mpu9250-9Axies-Motion-Sensor-Core-Development-Kit-Extensible-IoT-Development-Board/3226069_32836393710.html?spm=2114.12010615.8148356.12.25e96be7zRik8r.html)**&nbsp;&nbsp;&nbsp;:clapper:**[Related Video](#Related-Video)**

## Description

**M5Core GRAY** is a development kit based on ESP32 chip composed of a gray M5Core and a Bottom Base board. You can even program The M5Core GRAY through Blockly, Arduino or MicroPython.

The M5Core GRAY equips the ESP32 with everything necessary to program, run and develop on the wonderchip. It also features a MEMS Chip(**MPU9250**), and a TF  `T LCD, so you can create a 3D remote gesture controller, a simple "Leap Motion" via M5Core GRAY in a day in stead of couple weeks and so on.

The a Bottom board on the back of M5Core. It's designed for expanding gpio on M-Bus besides I2S Pins(GPIO0, GPIO12, GPIO13, GPIO15, GPIO34)for DIY. Each gpio on M-Bus is expanded as pin and port for convenience and flexibility.

## Feature

-  Programming Support: [UiFlow](http://flow.m5stack.com), [MicroPython](http://micropython.org/) and [Arduino](http://www.arduino.cc)
-  TF Card Support(Up to 16GB)

## PinMap

*We have several kinds of m5core board on sale, click [here](https://github.com/m5stack/M5-Schematic/blob/master/Core/hardware_diff_between_m5cores.md) for their difference.*

#### MainBoard Pinmap

**LCD & TF Card**

*LCD Pixel：320x240*
*Maximum storage of TF Card: 16GB*

<table>
 <tr><td>ESP32 Chip</td><td>GPIO23</td><td>GPIO19</td><td>GPIO18</td><td>GPIO14</td><td>GPIO27</td><td>GPIO33</td><td>GPIO32</td><td>GPIO4</td></tr>
 <tr><td>ILI9341(LCD Driver)</td><td>/</td><td>MISO</td><td>CLK</td><td>CS</td><td>DC</td><td>RST</td><td>BL</td><td> </td></tr>
 <tr><td>TF Card</td><td>MOSI</td><td>MISO</td><td>CLK</td><td> </td><td> </td><td> </td><td> </td><td>CS</td></tr>
</table>

**Button & Speaker**

<table>
 <tr><td>ESP32 Chip</td><td>GPIO39</td><td>GPIO38</td><td>GPIO37</td><td>GPIO25</td></tr>
 <tr><td>Button</td><td>BUTTON A</td><td>BUTTON B</td><td>BUTTON C</td></tr>
 <tr><td>Speaker</td><td> </td><td> </td><td> </td><td>Speaker Pin</td></tr>
</table>

**GROVE A**

<table>
 <tr><td>ESP32 Chip</td><td>GPIO22</td><td>GPIO21</td><td>5V</td><td>GND</td></tr>
 <tr><td>GROVE A</td><td>SCL</td><td>SDA</td><td>5V</td><td>GND</td></tr>
</table>

**9-axis IMU sensor(MPU9250)**

*I2C Address: 0x68*

<table>
 <tr><td>ESP32 Chip</td><td>GPIO22</td><td>GPIO21</td><td>5V</td><td>GND</td></tr>
 <tr><td>MPU9250</td><td>SCL</td><td>SDA</td><td>5V</td><td>GND</td></tr>
</table>

#### M5GO Base Pinmap

**GROVE B**

<table>
 <tr><td>ESP32 Chip</td><td>GPIO36</td><td>GPIO26</td><td>5V</td><td>GND</td></tr>
 <tr><td>GROVE B</td><td>GPIO36</td><td>GPIO26</td><td>5V</td><td>GND</td></tr>
</table>

**GROVE C**

<table>
 <tr><td>ESP32 Chip</td><td>GPIO16</td><td>GPIO17</td><td>5V</td><td>GND</td></tr>
 <tr><td>GROVE C</td><td>RXD</td><td>TXD</td><td>5V</td><td>GND</td></tr>
</table>

**LED Bar & MicroPhone**

<table>
 <tr><td>ESP32 Chip</td><td>GPIO15</td><td>GPIO34</td></tr>
 <tr><td>LED Bar</td><td>SIG Pin</td><td> </td></tr>
 <tr><td>MicroPhone</td><td> </td><td>MIC Pin</td></tr>
</table>

## PARAMETER

<table>
   <tr style="font-weight:bold">
      <td>M5Core Source</td>
      <td>Parameter</td>
   </tr>
   <tr>
      <td>ESP32</td>
      <td>240MHz dual core, 600 DMIPS, 520KB SRAM, Wi-Fi, dual mode Bluetooth</td>
   </tr>
   <tr>
      <td>Flash</td>
      <td>4MB</td>
   </tr>
   <tr>
      <td>Input</td>
      <td>5V @ 500mA</td>
   </tr>
   <tr>
      <td>Interface</td>
      <td>TypeC x 1, GROVE(I2C+I/0+UART) x 1</td>
   </tr>
   <tr>
      <td>LCD</td>
      <td>2 inch, 320x240 Colorful TFT LCD, ILI9342</td>
   </tr>
   <tr>
      <td>Speaker</td>
      <td>1W-0928</td>
   </tr>
      <tr>
      <td>Microphone</td>
      <td>MEMS Analog BSE3729 Microphone</td>
   </tr>
   <tr>
      <td>LED</td>
      <td>SK6812 3535 RGB LED x 10</td>
   </tr>
   <tr>
      <td>MEMS</td>
      <td>MPU9250</td>
   </tr>
   <tr>
      <td>Battery</td>
      <td>550mAh @ 3.7V, inside  vb</td>
   </tr>
   <tr>
      <td>Op.Temp.</td>
      <td>32°F to 104°F ( 0°C to 40°C )</td>
   </tr>
   <tr>
      <td>Size</td>
      <td>54 x 54 x 12.5 mm</td>
   </tr>
   <tr>
      <td>C.A.S.E</td>
      <td>Plastic ( PC )</td>
   </tr>
   <tr>
      <td>Weight</td>
      <td>120g with bottom, 100g only core</td>
   </tr>
</table>

## Include

-  1x M5Core GRAY
-  1x M5Core Bottom
-  Type-C USB Cable
-  User Manual

## Related Link

-  **Datasheet** - [ESP32](https://www.espressif.com/sites/default/files/documentation/esp32_datasheet_cn.pdf) - [MPU9250](http://www.invensense.com/wp-content/uploads/2015/02/PS-MPU-9250A-01-v1.1.pdf)

-  **Datasheet** - [ESP32](https://www.espressif.com/sites/default/files/documentation/esp32_datasheet_cn.pdf)

## Related Video

**m5stack instroduce**

<iframe width="560" height="315" src="https://www.youtube.com/embed/W5ZfDCBc1lk" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

**M5Core Cases**

[![core_bottom_01.png](http://m5-docs.oss-cn-shenzhen.aliyuncs.com/assets/img/case_img/core_compass.png)](https://v.youku.com/v_show/id_XNDAxNDI4MDM0OA==.html?spm=a2hzp.8253869.0.0)[![core_bottom_01.png](http://m5-docs.oss-cn-shenzhen.aliyuncs.com/assets/img/case_img/core_imu.png)](https://v.youku.com/v_show/id_XNDAxNDMwMjAyNA==.html?spm=a2hzp.8253869.0.0)[![core_bottom_01.png](http://m5-docs.oss-cn-shenzhen.aliyuncs.com/assets/img/case_img/core_avatar.png)](https://v.youku.com/v_show/id_XNDAxNDI3OTgwMA==.html?spm=a2hzp.8253869.0.0)

[![core_bottom_01.png](http://m5-docs.oss-cn-shenzhen.aliyuncs.com/assets/img/case_img/core_voice_recognition.png)](https://v.youku.com/v_show/id_XNDAxNDMwNzU5Mg==.html?spm=a2hzp.8253869.0.0)[![core_bottom_01.png](http://m5-docs.oss-cn-shenzhen.aliyuncs.com/assets/img/case_img/core_smart_electric_monitor.png)](https://v.youku.com/v_show/id_XNDAxNDI4NTQ0NA==.html?spm=a2hzp.8253869.0.0)[![core_bottom_01.png](http://m5-docs.oss-cn-shenzhen.aliyuncs.com/assets/img/case_img/core_smart_home.png)](https://v.youku.com/v_show/id_XNDAxNDMxMzg2MA==.html?spm=a2hzp.8253869.0.0)

[![core_bottom_01.png](http://m5-docs.oss-cn-shenzhen.aliyuncs.com/assets/img/case_img/core_leap_motion.png)](https://v.youku.com/v_show/id_XNDAxNDI4MjU5Mg==.html?spm=a2hzp.8253869.0.0)[![core_bottom_01.png](http://m5-docs.oss-cn-shenzhen.aliyuncs.com/assets/img/case_img/core_microphone_alexa.png)](https://v.youku.com/v_show/id_XNDAxNDMwNTYxNg==.html?spm=a2hzp.8253869.0.0)[![core_bottom_01.png](http://m5-docs.oss-cn-shenzhen.aliyuncs.com/assets/img/case_img/core_robot.png)](https://v.youku.com/v_show/id_XNDAxNDI4NDk3Ng==.html?spm=a2hzp.8253869.0.0)
