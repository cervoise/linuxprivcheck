# linuxprivcheck
Python script for privilege escalation for Linux

Original author is Mike Czumak (T_v3rn1x) -- @SecuritySift.

## Scripts

* old-linuxprivchecker.py: Famous linuxprivchecker.py (Python) with updates - I'll not update it anymore.
* linuxprivchecker3.py: Famous linuxprivchecker.py, compatible both Python 2 & 3 with updates.

## Options

The *--fast* does not perform check for passwords in .sh files.

## What's new

 * Support both Python 2 and 3 in one script 
 * Add tips (jail escape) and ressources (links)
 * Correction for broken links
 * Support *ip* and *ss* for new Linux versions
 * Add a fast options (avoid check for passwords in .sh files)
 * New check for:
   * Capabilities
   * Screen and Tmux opened shells
   * Current user is member of docker group (https://fosterelli.co/privilege-escalation-via-docker.html)
   * Check for passwords in .sh scripts
   * Check for SSH agent connexion in /tmp (https://www.clockwork.com/news/2012/09/28/602/ssh_agent_hijacking/)
 * Improve exploits part:
   * New exploits added (however I recommand to use a more complete tool for this part)
   * Correct versions for previous exploit to avoid false positives

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
