# USB Connection Logger
<p align="center">
    <img src="https://img.shields.io/badge/License-MIT-blue.svg" />
    <img src="https://img.shields.io/badge/Made%20with-Python-yellow.svg" />
</p>
This is a program that record entries of USB device connection to your computer and outputs it to a log file.

This can be used for investigations like logging if an external threat tried/has exfiltrated data or inputted a [malicious USB device](https://hakshop.com/products/usb-rubber-ducky-deluxe).

## Install and Running
You will need to have python3 install along with the [libusb driver](https://libusb.info) for your operating system.

First download the libraries:
```
pip3 install -r requirements.txt
```
Then run the program:
```
python3 usbLogger.py
```
## Compiling
If you want the program to run in the background without a the python console running, you will need to have pyinstaller installed.

Then
```
pyinstaller usbLogger.py --onefile --no-window --noconsole
```

## Example Log:
```python
2018-06-30 01:49:26: "Bus 020 Device 033: ID 154b:005b" has CONNECTED
2018-06-30 01:49:30: "Bus 020 Device 033: ID 154b:005b" has DISCONNECTED
2018-06-30 01:49:35: "Bus 020 Device 034: ID 1050:0116" has CONNECTED
2018-06-30 01:49:36: "Bus 020 Device 034: ID 1050:0116" has DISCONNECTED
2018-06-30 01:49:53: "Bus 020 Device 035: ID 05e3:0610" has CONNECTED
2018-06-30 01:49:53: "Bus 000 Device 001: ID 05e3:0616" has CONNECTED
2018-06-30 01:49:55: "Bus 000 Device 001: ID 05e3:0616" has DISCONNECTED
2018-06-30 01:49:55: "Bus 000 Device 002: ID 05e3:0616" has CONNECTED
2018-06-30 01:50:06: "Bus 020 Device 036: ID 154b:005b" has CONNECTED
2018-06-30 01:50:12: "Bus 020 Device 037: ID 1050:0116" has CONNECTED
2018-06-30 01:50:16: "Bus 020 Device 035: ID 05e3:0610" has DISCONNECTED
2018-06-30 01:50:16: "Bus 020 Device 036: ID 154b:005b" has DISCONNECTED
2018-06-30 01:50:16: "Bus 000 Device 002: ID 05e3:0616" has DISCONNECTED
2018-06-30 01:50:17: "Bus 020 Device 037: ID 1050:0116" has DISCONNECTED
```
