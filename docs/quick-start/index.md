# JS-Board quick start

Seeing JS-Board in action takes only a couple of steps:

1. Locate your favorite ESP32 device and connect it to your computer using a USB cable.
2. Open a Chrome or Edge web browser on Linux/MacOS/Windows and navigate to
   [http://js-board.github.io/flash](http://js-board.github.io/flash).
3. Follow the instructions on the page to flash your device with JS-Board (this use WebSerial).
4. Once the device is flashed, it will reboot and you can configure it in the web browser to
   connect to your WiFi network.
5. Once the device is connected to your WiFi network, you can click through to the device's
   web interface and start exploring.

## ESP32 device

Currently JS-Board is only compatible with "standard" ESP32 devices, i.e., no ESP32-C3, ESP32-S3, etc.
Support for these will follow...

## Browser

The web flashing uses the WebSerial API, which is currently only supported by Chrome and Edge.
Other browsers derived from Chrome (Brave, Vivaldi, et.al) should also work.
Firefox will definitely not work (they pretty much refuse supporting any API that accesses local
machine resources, oh well...)
Open [http://js-board.github.io/flash](http://js-board.github.io/flash).

## Flashing

The code on the web page uses the WebSerial API to let you choose the serial port to which
your ESP32 is attached.
It then erases the flash and proceeds to program the device with the JS-Board firmware.
It uses the same protocol as the command-line
[https://docs.espressif.com/projects/esptool/en/latest/esp32/installation.html](esptool.py) utility.

If you are having difficulties with the web flashing, you can also install esptool.py.
Under linux your package manager most likely has a package for it and that would be the
recommended option.
The alternative is to follow the directions on the esptool.py page to install it using pip.

## Configuration

Once the device is flashed, it will connect to the web flasher and be ready for configuration
asking you to connect it to your WiFi network.
Once connected to wifi the web page will provide a link to the web interface where you can
start managing the device and uploading your application.

If you flashed the device using esptool.py you will need to connect to the device's WiFi
access point (the SSID is of the form `JSB_XXXXXX`) and then navigate to `http://192.168.4.1/`.
When you connect to the access point the device provides a captive portal which should cause
your operating system to bring up a browser to authenticate with the network (this is designed
for public access points where yuo have to agree to terms of service to get internet access).
This browser is typically limited bu should work to get your device onto your local wifi.
