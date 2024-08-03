# ESPHome + ESP32-S3 Zero
ESP32-S3 Zero boards ([Waveshare branded](https://www.waveshare.com/wiki/ESP32-S3-Zero) and clones) need some extra configuration to work properly with ESPHome. 

See the yaml file for an example, including:

* board configuration
* fixing the WiFi auth error that prevents the device from connecting to WiFi and results in messages like this:
  ```
  [wifi_esp32:670]: Event: Disconnected ssid='[redacted]' bssid=[redacted] reason='Auth Expired' [08:45:07][W][wifi:652]: Error while connecting to network.
  ```
* support for the WS2812 RGB LED

# Flashing

When flashing for the first time, make sure you: 1) hold the `boot` button 2) press and release the `reset` button 3) release `boot`. The device file didn't show up in `/dev/ttyXXX` in Linux for me, so I flashed in Windows using the [ESPHome WebFlasher](https://web.esphome.io/).
