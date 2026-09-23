# SocialSpeaker
A RaspberyPi/ESP-32 based portable battery powered speaker, with the ability the map custom macros to physical buttons

## What is it
* Two ESP32-32 3.5" 340x480 LCD Resistance Touch Boards
* RaspberryPI 4 model B (4gb)
* Inland 1602  I2C display
* Three  [Rotary Encoder + 1.3 inch OLED Display White](https://www.amazon.com/dp/B0F32CBZ3N?ref=ppx_yo2ov_dt_b_fed_asin_title/ "Rotary Encoder + 1.3 inch OLED Display White")
* Eight mechanical keyboard switches
* Six EC11 rotary encoders
  You might be thinking why use RPI and ESP32, and its because I had it laying around, everything but the encoders and expansion, so the hardware design philosophy is "i had it around"

## Architecture
#### RaspberryPi - The brain, connects to external wi-fi, hosts AP for esp32 boards, hosts server for esp32/rpi coms and stores all profile based logic locally
#### Two ESP32-32E dumb I/O displays, they send input events to the RPI and renders whatever the RPI tells it too, pretty much zero logic going on the ESP32 board

## Profiles
Profiles are the modes or settings, you can create really anything the hardware can handle, (assuming you can make it with python) , they live all on the PI

