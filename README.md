# linuxprivcheck
Python script for privilege escalation for Python

Original author is Mike Czumak (T_v3rn1x) -- @SecuritySift.

## Scripts

* linuxprivchecker.py: Famous linuxprivchecker.py with updates
* linuxprivchecker3.py: Famous linuxprivchecker.py for Python 3 with updates

## Known issues
* Python 3 version is not able to find superuser.
* No real Licence is defined (https://github.com/cervoise/linuxprivcheck/issues/1)

## What if Python is not on the target?

On Kali (or other Linux) install pyinstaller :

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

## Help

If you need help with SUID and cronjob lists check this repo: https://github.com/cervoise/suid-bin/
