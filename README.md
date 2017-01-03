# Digistump Oak development platform for [PlatformIO](http://platformio.org)

> WIP!

Based on [framework-espressif8266](https://github.com/platformio/platform-espressif8266) using [OakCore](https://github.com/digistump/oakcore)'s config for the Arduino IDE.

## Motivation

- [platformio/platformio-core#445](https://github.com/platformio/platformio-core/issues/445)
- Arduino IDE is cool if you're learning how to code.
- Particle's cloud IDE was written for the same audience.
- More importantly, the Particle cloud IDE places useless (to me) restrictions on library structure.

## Demotivation

Maybe it's easier to just forget about OTA and upload using esptool.

## TODO

- [x] Create `platform.json`
- [x] Create manifest
- [x] Create board definition
- [x] Create framework builder
- [ ] Make `builder/main.py` work
- [ ] Default to OTA uploads (*how?*)
- [ ] Allow selection of Particle device by ID (in `platformio.ini`)
- [ ] Repackage packages with `package.json` files (`pio` won't install w/o these):
  - [ ] [OakCLI](https://github.com/digistump/oakcli)
  - [ ] [esptool2](https://github.com/digistump/esptool2)
  - [ ] [OakCore](https://github.com/digistump/oakcore)
- [ ] Implement other Oak variants

Later:

Implement a more general solution for Particle.  Instead of using OakCLI, we *should* be able to just use [particle-cli](https://npmjs.com/package/particle-cli).  Maybe it can be packaged with `nexe` like OakCLI?  Don't think forcing Node.js to be installed would be appropriate.

Serving the prebuilt binaries on bintray.com.

## Author

:copyright: 2016 Christopher Hiller.  Licensed MIT.
