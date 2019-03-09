# XPS-9360-Hackintosh

EFI and Tools for macOS on Dell XPS 9360 i5-8250U 

## Installation

-Use [etcher](https://www.balena.io/etcher/) and [dmg](https://mirrors.dtops.cc/iso/MacOS/daliansky_macos/) to install MacOS

## Usage

- Boot with `DVMT.efi` in `/CLOVER/tools`, use command `setup_var` to modify some [UEFI Variables](https://github.com/the-darkvoid/XPS9360-macOS#uefi-variables)

- After installation, use `XPS9360.sh` with option `--patch-hda` in folder `Other` to inject AppleHDA 

- Run `/other/HIDPI/run.command` to open HIDPI or use：
  ```
   sh -c "$(curl -fsSL https://raw.githubusercontent.com/xzhih/one-key-hidpi/master/hidpi-zh.sh)"
  ```

- Change your [`Serial Number`, `Custom UUID`](https://www.tonymacx86.com/threads/an-idiots-guide-to-imessage.196827/)by Clover Configurator

## Hints

- If you fail to boot, change `platform-id` to `0x12345678`.

- Don't set the parameters in config.plist if you don't understand it.

- Rebuild cache use `kext utility` or commands:

<pre name="code" class="bash">
#!/bin/sh
sudo chmod -Rf 755 /S*/L*/E*
sudo chown -Rf 0:0 /S*/L*/E*
sudo chmod -Rf 755 /L*/E*
sudo chown -Rf 0:0 /L*/E*
sudo rm -Rf /S*/L*/PrelinkedKernels/*
sudo rm -Rf /S*/L*/Caches/com.apple.kext.caches/*
sudo touch -f /S*/L*/E*
sudo touch -f /L*/E*
sudo kextcache -Boot -U /
</pre>

## Credits

### [the-darkvoid](https://github.com/the-darkvoid/XPS9360-macOS)

### [ymmshi](https://github.com/ymmshi/XPS-9360)

### [xzhih](https://github.com/xzhih/one-key-hidpi)

### [daliansky](https://blog.daliansky.net/)
