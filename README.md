# Sense-NET

**Sense-NET** is a tool to interact with bioimplants, specifically those manufactured by [Dangerous Things](https://dangerousthings.com/). It is designed to work with Unix systems and provides functionalities for both NFC and RFID modes, such as reading, writing, and retrieving implant information.

---

## Features

- **RFID Mode**:
  - Retrieve implant information using compatible RFID readers.
- **NFC Mode**:
  - Retrieve implant UID, manufacturer, checksum, and payload.
  - Read and parse NDEF messages.
  - Write new NDEF content to implants.
  - Read raw implant memory blocks (up to 48 blocks).

---

## System Requirements

- **Operating System** 
  - macOS.
  - *BSD.
  - Linux.
- **Implant Compatibility**:
  - [NExT Implant](https://dangerousthings.com/product/next/).
  - [xSIID Implant](https://dangerousthings.com/product/xsiid/).
  - [xHT Implant](https://dangerousthings.com/product/xht/).
  - [xSLX Implant](https://dangerousthings.com/product/xslx/).
  - [xNT Implant](https://dangerousthings.com/product/xnt/).
  - [xEM Implant](https://dangerousthings.com/product/xem/).
  - [xDF2 Implant](https://dangerousthings.com/product/xdf2/).
  - [VivoKey Spark](https://dangerousthings.com/product/vivokey-spark/).
- **Reader Compatibility**:
  - [Dangerous Things RFID Reader (Sycreader RFID Technology / AuthenTec)](https://dangerousthings.com/product/kbr1/).
  - [ACR1252 Dual Reader (ACS)](https://www.acs.com.hk/en/products/342/acr1252u-usb-nfc-reader-iii-nfc-forum-certified-reader/).

---

## Sense/Net as an executable

A redistributable package with dependencies included is available, compiled with PyInstaller. It can be found on the `dist` directory.

```bash
cd dist/
chmod +x sense-net
./sense-net
```

---

## Sense/Net as an independent Python tool

The project requires Python 3 and the following Python libraries:

```
ndef
pyscard
termcolor
```

Ensure you have these dependencies installed. You can do so by running:

```bash
pip install -r requirements.txt
python3 sense-net.py
```

Follow the prompts to interact with your bioimplant.

---

## Usage

Whether using the Python version or the redistributable one, and with either an RFID or NFC reader, Sense/Net can be run interactively or by directly invoking the desired option:

```bash
Sense-NET: A tool for interacting with bioimplants.

options:
  -h, --help                  show this help message and exit
  --get-rfid-info             Get RFID implant information.
  --get-nfc-info              Get NFC implant information.
  --read-ndef                 Read NDEF contents from an NFC implant.
  --read-raw                  Read raw blocks from an NFC implant.
  --write-ndef MESSAGE        Write NDEF content to an NFC implant.
  --version                   Get Sense/Net version.

```

---

## Screenshots

### NFC Example
<img src="img/A.png" alt="NFC Example" width="600">

### Reading NDEF Data
<img src="img/B.png" alt="NDEF Data" width="600">

### Reading Raw Data
<img src="img/C.png" alt="Raw Data" width="600">

### RFID Example
<img src="img/D.png" alt="RFID Example" width="600">

---

## Credits

This work is based on original contributions from [VladoPortos](https://github.com/VladoPortos) who actually wrote [the only working library for ACR1252](https://rpi4cluster.com/python-nfc-writer-reader/).

---

## Contributing

Feel free to submit issues or pull requests to enhance the functionalities or expand compatibility to other platforms and devices.