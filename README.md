# ESP Home Pool Temperature 🌡️
ESPHome configuration to create a pool temperature sensor which reports via MQTT and HASSIO

![Maintenance](https://img.shields.io/maintenance/yes/2023)
![GitHub](https://img.shields.io/github/license/virtuallytd/esphome-pooltemp)
![GitHub issues](https://img.shields.io/github/issues/virtuallytd/esphome-pooltemp)

![GitHub commit activity](https://img.shields.io/github/commit-activity/y/virtuallytd/esphome-pooltemp)
![GitHub last commit](https://img.shields.io/github/last-commit/virtuallytd/esphome-pooltemp)
![GitHub contributors](https://img.shields.io/github/contributors/virtuallytd/esphome-pooltemp)

ESPHome Pool Temperature Monitoring Project

The "ESPHome Pool Temperature Monitoring" project aims to provide a solution to track and monitor pool temperature using the ESPHome platform and a Dallas temperature sensor all powered by battery. It integrates with your Home Assistant system, allowing you to view and interact with the data collected from your pool.

The core of the system is an ESP8266 board (specifically, the NodeMCU variant). It hosts a Dallas temperature sensor connected via GPIO2, which measures the pool's temperature and reports it back to the Home Assistant through the MQTT protocol or direct via the Home Assistant API integration. The device also monitors its power level using the ADC function, providing insights about its power state of the battery (LiFePO4).

The device is designed to operate in a low power mode, using the deep sleep capabilities of the ESP8266. It sleeps for 60 minutes and then wakes up for a brief period to take measurements and send the data to the server. The deep sleep cycle is customizable through a Home Assistant Boolean flag, allowing you to prevent the device from entering deep sleep mode when necessary for troubleshooting or upgrades (OTA).
