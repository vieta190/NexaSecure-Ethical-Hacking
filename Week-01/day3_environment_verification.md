# Day 3: Hypervisor & Kali Linux Setup

## 1. Environment Specifications
- **Hypervisor:** Oracle VirtualBox
- **Guest Operating System:** Kali GNU/Linux Rolling 2026.2 (64-bit)
- **Resource Allocation:** 2 vCPUs | 2 GB RAM (1969 MB) | 80 GB Storage (`/dev/sda1`)
- **Network Adapter Mode:** NAT (`10.0.2.15/24`)

## 2. Technical Analysis & Parameter Verification
- **Processor Allocation (`nproc`):** The output `2` verifies that 2 virtual CPU cores are assigned to the guest instance to ensure adequate multithreading performance during active security testing.
- **Memory Provisioning (`free -m`):** The output displays `1969 MB` usable RAM out of the total `2048 MB` (2 GB) allocated in VirtualBox settings, accounting for underlying hypervisor overhead.
- **Storage Capacity (`df -h /`):** The root partition (`/dev/sda1`) reflects a total capacity of `79G` (~80 GB) with `16G` used and `59G` available, providing ample disk space for dynamic lab tool deployments and logging.
- **Kernel & OS Release (`lsb_release -a` & `uname -a`):** Confirms the running system is **Kali GNU/Linux Rolling 2026.2** on a 64-bit architecture (`x86_64`) backed by Linux kernel version `6.19.14+kali1`.
- **Network Configuration (`ip -4 a`):** Interface `eth0` receives `10.0.2.15/24` via VirtualBox's internal NAT network engine, guaranteeing outbound internet access for tool package updates.

## 3. System Verification Commands
```bash
nproc
free -m
df -h /
lsb_release -a
uname -a
ip -4 a
