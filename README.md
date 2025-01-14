# GPSTimeServerSolar

![ezgif com-gif-maker0](https://user-images.githubusercontent.com/38574378/117382664-69117f00-aeb5-11eb-818f-4dcee22dbfc9.gif)

Solar powered WiFi enabled GPS fed NTP server 
based on ESP32 Devkit and Arduino framework

Parts list:

- DOIT ESP32 DEVKIT V1
- DS3231 RTC
- Neo-6m V2 GPS
- 0.96" OLED Display
- DFROBOT 900mA MPPT Solar Panel Controller
- Solar panels 5v 500ma or larger 
- 18650 battery holder
- WS2812 LED
- Resistors as needed for LED
- Switch key and momentary push button

---
<p align="center"><img src="https://user-images.githubusercontent.com/38574378/132773469-08fb7b59-2f9d-4641-9665-c8d50d3904bc.png"><b>   ATTENTION   </b><img src="https://user-images.githubusercontent.com/38574378/132773469-08fb7b59-2f9d-4641-9665-c8d50d3904bc.png"></p> 

Several DS3231 modules being sold today contain a hazardous design flaw in which it supplies a voltage to the battery cradle regardless if it came with a rechargeable battery or not. If it came with a CR2032 battery (non-rechargeable) the consequence is that it will swell, explode, or worse. If it came with a LIR2032 battery (rechargeable), the module being fed with 5v will generate an unsafe charging voltage for that battery.

There are workarounds for that so you don't need to toss your module away, the most popular being removing a diode and/or resistor.

There's a long discussion on the thread below about root cause and possible fixes:

https://forum.arduino.cc/t/zs-042-ds3231-rtc-module/268862/33

---

Libraries:

-	paulstoffregen/Time@^1.6
-	makuna/RTC@^2.3.5
-	mikalhart/TinyGPS@0.0.0-alpha+sha.db4ef9c97a
-	olikraus/U8g2@^2.28.8

Source code based on:

- http://w8bh.net/avr/clock2.pdf
- https://forum.arduino.cc/t/ntp-time-server/192816
- https://www.linkedin.com/pulse/iot-maker-tale-stratum-1-time-server-built-from-scratch-monteiro/

![sketch_bb-menor](https://user-images.githubusercontent.com/38574378/117375890-66f3f400-aea6-11eb-9389-1b9b0b01f88f.png)
