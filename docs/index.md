# Introduction

JS-Board is a Javascript firmware that runs on ESP32 microcontrollers to simplify the
development and deployment of applications.
It uses the Moddable SDK and facilitates configuring devices, uploading new applications as mods,
and performing general troubleshooting.
The primary interface for JS-Board is a web app served by the device itself over WiFi.

The goal of JS-Board is to support the following use-cases:

- Develop applications on a WiFi-attached device without having to connect a USB cable.
- Interactively explore the device's capabilities and troubleshoot problems using a
  web-based REPL (read-print-eval loop).
- Deploy new devices by flashing them with JS-Board from the web browser and then
  upload your application.
- Manage deployed devices through their web interface.

## License

JS-Board uses the Apache 2.0 license, which means everything is free.
