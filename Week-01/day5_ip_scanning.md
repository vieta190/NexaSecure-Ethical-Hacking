# Day 5: IP Configuration & Local Network Scanning

## Summary
* **Network Inspection:** Enumerated interface states (`ip a`), gateway routes (`ip route`), and DNS resolution (`nslookup`).
* **Host Discovery:** Conducted ARP-based local network discovery (`netdiscover`) and ICMP echo checks (`ping`).

## Execution Log
bash
ip a
ip route
nslookup google.com
sudo netdiscover -r 10.0.2.0/24 -c 3
ping -c 3 10.0.2.2
## Evidence
![IP & Routing Configuration](screenshots/day5_kali1.png)
![DNS Resolution & Ping Test](screenshots/day5_kali2.png)
![Netdiscover Local Host Discovery](screenshots/day5_kali3.png)
