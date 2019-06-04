<a href="https://www.bigclown.com/"><img src="https://bigclown.sirv.com/logo.png" width="200" alt="BigClown Logo" align="right"></a>

# Firmware for BigClown Lora ČRA Ještěd - 3D Model

[![Travis](https://img.shields.io/travis/bigclownprojects/bcf-lora-cra-jested/master.svg)](https://travis-ci.org/bigclownprojects/bcf-lora-cra-jested)
[![Release](https://img.shields.io/github/release/bigclownprojects/bcf-lora-cra-jested.svg)](https://github.com/bigclownprojects/bcf-lora-cra-jested/releases)
[![License](https://img.shields.io/github/license/bigclownprojects/bcf-lora-cra-jested.svg)](https://github.com/bigclownprojects/bcf-lora-cra-jested/blob/master/LICENSE)
[![Twitter](https://img.shields.io/twitter/follow/BigClownLabs.svg?style=social&label=Follow)](https://twitter.com/BigClownLabs)

## Description

Unit measure temperature, relative humidity and atmospheric pressure.
Values is sent every 15 minutes over LoRaWAN. Values are the arithmetic mean of the measured values since the last send.

Measure interval is 30s.

## Buffer
big endian

| Byte    | Name        | Type   | multiple | unit
| ------: | ----------- | ------ | -------- | -------
|       0 | HEADER      | uint8  |          |
|  1 -  2 | TEMPERATURE | int16  | 10       | °C
|       3 | HUMIDITY    | uint8  | 2        | %
|  4 -  5 | PRESSURE    | uint16 | 0.5      | Pa

### Header

* 0 - bool
* 1 - update
* 2 - button click
* 3 - button hold

## AT Interface

```sh
picocom -b 115200 --omap crcrlf  --echo /dev/ttyUSB0
```

## License

This project is licensed under the [MIT License](https://opensource.org/licenses/MIT/) - see the [LICENSE](LICENSE) file for details.

---

Made with &#x2764;&nbsp; by [**HARDWARIO s.r.o.**](https://www.hardwario.com/) in the heart of Europe.