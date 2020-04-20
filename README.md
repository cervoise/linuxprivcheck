# linuxprivcheck
Python script for privilege escalation for Linux

Original author is Mike Czumak (T_v3rn1x) -- @SecuritySift.

## Scripts

* old-linuxprivchecker.py: Famous linuxprivchecker.py (Python) with updates - I'll not update it anymore.
* linuxprivchecker3.py: Famous linuxprivchecker.py, compatible both Python 2 & 3 with updates.

## Options

The *--fast* does not perform check for passwords in .sh files.

## Known issues
* No real Licence is defined (https://github.com/cervoise/linuxprivcheck/issues/1).

## What if Python is not on the target?

On Kali (or other Linux) install pyinstaller:

```bash
$ pip install pyinstaller
$ pip3 install pyinstaller
```

Then compile the script:

```bash
$ python -m PyInstaller --onefile linuxprivchecker.py
$ python3 -m PyInstaller --onefile linuxprivchecker3.py
```

Standalone ELF will be in *./dist/*

### Known issues
 * Will not work if the libc version needed is not on your target 

## Help

If you need help with SUID and cronjob lists check this repo: https://github.com/cervoise/suid-bin/ or this project: https://github.com/TH3xACE/SUDO_KILLER.

If you need to find passwords you can look on https://github.com/AlessandroZ/LaZagne or https://github.com/0xmitsurugi/gimmecredz.
