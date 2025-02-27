# waveshare-7inch
# ESP32-S3-Touch-LCD-7

ADD bussynonna-panel.yaml to esphome config

# waveshare-7inch
# ESP32-S3-Touch-LCD-7
substitutions:
  name: "bussynonna-panel"
  friendly_name: "Bussynonna Panel"
  room: "Bus"

# Wifi Setup
wifi:
  ssid: !secret wifi_ssid
  password: !secret wifi_password

# Packages
packages:
  setup:
    url: https://github.com/weswark/waveshare-7inch/
    files: [device/esp32-s3-touch-lcd-7.yaml,
            addon/time.yaml,
            addon/backlight.yaml,
            addon/network.yaml,
            assets/fonts.yaml,
            assets/icons.yaml,
            assets/images.yaml,
            theme/button.yaml,
            panels/bus-sensors.yaml,
            panels/bus-lvgl.yaml]
    refresh: 1sec
