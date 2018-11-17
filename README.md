# XPS-9360-Hackintosh

EFI and Tools for macOS on Dell XPS 9360 i5-8250U 

## Usage

- Boot with `DVMT.efi` in `/CLOVER/tools`, use command `setup_var` to modify some [UEFI Variables](https://github.com/the-darkvoid/XPS9360-macOS#uefi-variables)

- After installation, use `XPS9360.sh` with option `--patch-hda` in folder `Other` to inject AppleHDA 

- Run `/other/HIDPI/run.command` to open HIDPI or use：
  ```$ sh -c "$(curl -fsSL https://raw.githubusercontent.com/xzhih/one-key-hidpi/master/hidpi-zh.sh)"```

- Change your [`Serial Number`, `Custom UUID`](https://www.tonymacx86.com/threads/an-idiots-guide-to-imessage.196827/)by Clover Configurator

## Credits

### [the-darkvoid](https://github.com/the-darkvoid/XPS9360-macOS)

### [ymmshi](https://github.com/ymmshi/XPS-9360)

### [xzhih](https://github.com/xzhih/one-key-hidpi)
