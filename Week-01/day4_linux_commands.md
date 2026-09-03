# Day 4: Linux Command Line Proficiency

## 1. Directory Navigation & Workspace Management
- **Directory Verification (`pwd`):** Confirmed active path as `/home/kali`.
- **Workspace Provisioning (`mkdir -p ~/day4_practice/test_dir`):** Recursively created dedicated practice structure without impacting parent directories.
- **Context Switch (`cd ~/day4_practice`):** Shifted execution environment to the newly generated lab directory.
- **Detailed Listing (`ls -la`):** Verified directory structure and file attributes including standard hidden nodes (`.` and `..`).

## 2. File Operations & Text Processing
- **File Initialization (`echo ... > target.txt`):** Created `target.txt` with initial header content.
- **Content Appending (`echo -e ... >> target.txt`):** Utilized escape sequences (`\n`) to append structured port state strings.
- **File Output (`cat target.txt`):** Displayed complete file contents directly to standard output.
- **Pattern Filtering (`grep "open" target.txt`):** Filtered lines matching active services (`port 22: open` and `port 80: open`).
- **Line Truncation (`head -n 2 target.txt` / `head -n 1 target.txt`):** Extracted designated top lines from the file target.

## 3. File Permissions & Security Controls
- **Restrictive Mode (`chmod 600 target.txt`):** Updated permission bits to `-rw-------` (Read/Write for Owner only; zero access for Group and Others). Verified via `ls -l target.txt`.
- **Permissive Execution Mode (`chmod 755 target.txt`):** Reconfigured permission bits to `-rwxr-xr-x` (Full access for Owner; Read/Execute for Group and Others). Verified state change via `ls -l target.txt`.

## 4. System & Process Inspection
- **Process Enumeration (`ps aux | head -n 10`):** Piped standard process output to isolate system init and worker threads (`/sbin/init`, `kthreadd`).
- **Identity Verification (`whoami`):** Confirmed active terminal session user context as `kali`.
- **Kernel Release Check (`uname -r`):** Output `6.19.14+kali-amd64` confirmed system architecture and kernel version.

## 5. Executed Commands Summary
```bash
# Directory Management
pwd
mkdir -p ~/day4_practice/test_dir
cd ~/day4_practice
ls -la

# File & Text Operations
echo "nexasecure day 4 lab" > target.txt
echo -e "port 22: open\nport 80:open\nport 443:closed" >> target.txt
cat target.txt
grep "open" target.txt
head -n 2 target.txt
head -n 1 target.txt

# Permission Management
chmod 600 target.txt
ls -l target.txt
chmod 755 target.txt
ls -l target.txt

# System Inspection
ps aux | head -n 10
whoami
uname -r
