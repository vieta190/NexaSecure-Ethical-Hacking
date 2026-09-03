# Day 6: Install Metasploitable 2

## Summary
* **Target Deployment:** Configured Metasploitable 2 vulnerable Linux target VM on VirtualBox using Host-Only networking.
* **Network Verification:** Confirmed layer 3 reachability between Kali Linux (`192.168.56.104`) and Metasploitable 2 (`192.168.56.103`).
* **Remote Session Verification:** Established an active terminal shell session from Kali to the target host using default credentials (`msfadmin:msfadmin`).

## Execution Log
```bash
# Metasploitable IP Verification (Executed on Target VM)
ifconfig

# Network Reachability Check (Executed on Kali)
ping -c 3 192.168.56.103

# Remote Interactive Session (Executed on Kali)
telnet 192.168.56.103
```
