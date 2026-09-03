# Day 2: Networking Basics

## 1. TCP/IP Architecture Model
- **Application Layer:** Provides network services directly to end-user applications (Protocols: HTTP, HTTPS, SSH, DNS, FTP).
- **Transport Layer:** Manages end-to-end communication, session establishment, and error recovery using TCP (connection-oriented, guaranteed delivery) or UDP (connectionless, low latency).
- **Internet Layer:** Handles logical IP addressing, packet formatting, and routing across distinct networks using IPv4, IPv6, and ICMP.
- **Network Access Layer:** Translates network packets into physical signals and manages hardware MAC addressing across local network segments.

## 2. Domain Name System (DNS) Fundamentals
- **Purpose:** Resolves human-readable domain names (e.g., `target.local`) into machine-routable IP addresses (e.g., `192.168.56.102`).
- **Resolution Query Lifecycle:** Client $\rightarrow$ Local Cache $\rightarrow$ Recursive Resolver $\rightarrow$ Root Server $\rightarrow$ TLD Server $\rightarrow$ Authoritative Name Server.
- **Key Resource Records:**
  - **A Record:** Maps a hostname directly to an IPv4 address.
  - **AAAA Record:** Maps a hostname directly to an IPv6 address.
  - **CNAME Record:** Aliases one domain name to another canonical hostname.
  - **MX Record:** Specifies mail servers responsible for receiving email on behalf of a domain.
  - **TXT Record:** Stores arbitrary text, used for domain ownership validation and email authentication policies (SPF, DKIM, DMARC).

## 3. Key Ports & Services Matrix

| Port | Service | Transport Protocol | Default Usage | Security Considerations |
| :--- | :--- | :--- | :--- | :--- |
| **21** | FTP | TCP | File Transfer | Unencrypted; transmits credentials in cleartext |
| **22** | SSH | TCP | Secure Shell | Encrypted remote terminal management |
| **53** | DNS | UDP / TCP | Name Resolution | Primarily UDP; uses TCP for zone transfers or large payloads |
| **80** | HTTP | TCP | Web Server | Unencrypted web traffic |
| **443** | HTTPS | TCP | Secure Web Server | Encrypted web traffic protected via TLS/SSL |

## 4. HTTP Request & Response Cycle
- **Request:** Client sends HTTP method (`GET`, `POST`), URI path, headers (`Host`, `User-Agent`, `Cookie`), and optional body payload.
- **Response:** Server returns an HTTP status code (`200 OK`, `301 Moved Permanently`, `403 Forbidden`, `404 Not Found`, `500 Server Error`), headers (`Content-Type`, `Set-Cookie`), and payload content (HTML/JSON).
