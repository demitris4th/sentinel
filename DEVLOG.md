# **Devlog: sentinel Project**

A running log of what I built, what broke, and what I learned.  
---

# **Entries**

## \[27/07/2026\] Phase 0: Fresh Pi flash \+ SSH access

**Goal for this session:** Flash Raspberry Pi OS Lite, get headless SSH access working, lock down auth.

**What I did:**

- Flashed Raspberry Pi OS Lite (64-bit) via Raspberry Pi Imager, pre-configured hostname sentinel-pi, SSH enabled, custom username set via advanced options  
- Booted headless, connected via ssh demitris@sentinel-pi.local from cmd  
- Generated a dedicated SSH key for the Pi  
- Copied the public key generated using PowerShell since ssh-copy-id didnt work because it wasnt available on Window  
- Verified key-based login worked before disabling passwords, edited sshd\_config to turn off password authentication  
- Attempted to set a static IP using DHCP reservation but no access to admin router page (I live in a rental)  
- Ran apt update/upgrade, installed git and python3/venv/pip   
- Rebooted and checked everything survived

**What broke / errors hit:**

@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@

@    WARNING: REMOTE HOST IDENTIFICATION HAS CHANGED\!     @

@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@

...

Host key verification failed.

**How I fixed it:** Ran ssh-keygen \-R sentinel-pi.local to remove the stale host key entry from Windows' known\_hosts (leftover from a previous flash of the same hostname/IP)

**What I learned:** SSH host keys are tied to the hostname/IP, not the physical device, because reflashing the SD card generates a new key pair, so the client (correctly) flags it as a potential impersonation until I confirm it's expected. 

**Next up:** Initiate Phase 1 which is creating the Core Monitor (Python \+ SQLite)

---

---

## Weekly Retros

## Week of YYYY-MM-DD

**What did I actually finish this week?**

**What took longer than expected, and why?**

**What would I do differently?**

---

