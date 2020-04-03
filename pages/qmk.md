---
title: qmk
---

## initial setup
In my case, a simplified version of the setup in the `util/macos_install.sh` script from the qmk repo is necessary. In particular, pinning version 8 of avr-gcc neems unnecessary, saving a very lenghty compilation from source (the latest version is bottled).

```bash
brew tap osx-cross/avr
brew tap PX4/homebrew-px4
brew update
brew install avr-gcc gcc-arm-none-eabi dfu-util
```

## build and flash
Here's how I build and flash:

```bash
make planck/rev6:lepistone:dfu-util
make ergodox_ez:lepistone:teensy
```
