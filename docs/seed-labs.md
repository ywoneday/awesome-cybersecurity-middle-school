# SEED Security Labs — Detailed Guide

[SEED Labs](https://seedsecuritylabs.org/) (SEcurity EDucation) is a hands-on cybersecurity lab platform developed by Prof. Wenliang Du at Syracuse University. It provides 40+ labs across 7 categories, all freely available. Used by 1000+ schools in 65 countries.

---

## Lab Environment Setup

### Option 1: Pre-built VM (Recommended)

| Item | Details |
|---|---|
| **VM Image** | SEED Ubuntu 20.04 VirtualBox image (`SEED-Ubuntu20.04.zip`, 4.0 GB) |
| **Download** | [Google Drive](https://drive.google.com/file/d/138fqx0F8bThLm9ka8cnuxmrD6irtz_4m/view?usp=sharing) / [DigitalOcean](https://seed.nyc3.cdn.digitaloceanspaces.com/SEED-Ubuntu20.04.zip) |
| **MD5** | `f3d2227c92219265679400064a0a1287` |
| **VM Manual** | [How to install the pre-built VM](https://github.com/seed-labs/seed-labs/blob/master/manuals/vm/seedvm-manual.md) |
| **Requirements** | VirtualBox 6.x+, 4 GB RAM allocated to VM, 20 GB disk space |

### Option 2: Build VM from Scratch

Full instructions to build the SEED VM from a base Ubuntu 20.04 installation:
- [Build Guide](https://github.com/seed-labs/seed-labs/blob/master/manuals/vm/seedvm-from-scratch.md)

### Option 3: Apple Silicon (M1/M2) Macs

VirtualBox does not support Apple Silicon. Use VMware Fusion Player (free) instead:
- [ARM Setup Guide](https://github.com/seed-labs/seed-labs/blob/master/lab-setup/apple-arm/seedvm-fusion.md) (uses Ubuntu 22.04)
- [Lab Compatibility on ARM](https://github.com/seed-labs/seed-labs/blob/master/lab-setup/apple-arm/Lab_Testing.md)

### Option 4: Cloud VM

Run SEED labs on any cloud provider (Google Cloud, AWS, DigitalOcean, etc.):
- **Minimal specs:** 1 CPU, 2 GB RAM
- **Cost:** ~$0.25 per lab session on Google Cloud
- **Setup Guide:** [Cloud VM Manual](https://github.com/seed-labs/seed-labs/blob/master/manuals/cloud/seedvm-cloud.md)
- **Benefit:** Students can work from any device (phone, tablet, Chromebook) via VNC

---

## All Labs by Category

### Web Security (5 labs) — AP Unit 5

> ★★★ **Most accessible for middle school.** Labs use pre-built vulnerable web apps with step-by-step instructions. Students can see attacks work in real time.

| # | Lab | Description | PPT Slides | Lab Link |
|---|---|---|---|---|
| 1 | Cross-Site Scripting (XSS) | Launch XSS attacks on the Elgg social networking app; experiment with countermeasures like input validation and Content Security Policy. | [Slides](https://www.handsonsecurity.net/files/slides/W03_Web_XSS.pptx) | [Lab](https://seedsecuritylabs.org/Labs_20.04/Web/Web_XSS_Elgg/) |
| 2 | Cross-Site Request Forgery (CSRF) | Launch CSRF attacks on Elgg; experiment with countermeasures like anti-CSRF tokens and SameSite cookies. | [Slides](https://www.handsonsecurity.net/files/slides/W02_Web_CSRF.pptx) | [Lab](https://seedsecuritylabs.org/Labs_20.04/Web/Web_CSRF_Elgg/) |
| 3 | SQL Injection | Launch SQL injection attacks on a web application; experiment with prepared statements and other countermeasures. | [Slides](https://www.handsonsecurity.net/files/slides/W04_Web_SQL_Injection.pptx) | [Lab](https://seedsecuritylabs.org/Labs_20.04/Web/Web_SQL_Injection/) |
| 4 | Clickjacking | Launch clickjacking attacks on Alice's Cupcakes website; experiment with X-Frame-Options and CSP countermeasures. | [Slides](https://www.handsonsecurity.net/files/slides/W05_Web_Clickjacking.pptx) | [Lab](https://seedsecuritylabs.org/Labs_20.04/Web/Web_Clickjacking_Cupcakes/) |
| 5 | Shellshock | Exploit the Shellshock vulnerability (CVE-2014-6271) in Bash to attack a web server. | [Slides](https://www.handsonsecurity.net/files/slides/W06_Shellshock.pptx) | [Lab](https://seedsecuritylabs.org/Labs_20.04/Web/Shellshock/) |

---

### Cryptography (8 labs) — AP Unit 5

> ★★★ **Concepts are highly teachable** via the PPT slides. Select labs for hands-on practice. RSA, PKI, and hash labs align well with AP Unit 5 topics.

| # | Lab | Description | PPT Slides | Lab Link |
|---|---|---|---|---|
| 1 | Secret-Key Encryption | Explore secret-key encryption using OpenSSL: AES, modes of operation (ECB, CBC, CTR), IV, key derivation. | [Slides](https://www.handsonsecurity.net/files/slides/C01_Secret_Key_Encryption.pptx) | [Lab](https://seedsecuritylabs.org/Labs_20.04/Crypto/Crypto_Encryption/) |
| 2 | MD5 Collision Attack | Use MD5 collision to create two different programs with the same hash. Demonstrates weakness of MD5. | [Slides](https://www.handsonsecurity.net/files/slides/C02_One_Way_Hash.pptx) | [Lab](https://seedsecuritylabs.org/Labs_20.04/Crypto/Crypto_MD5_Collision/) |
| 3 | Hash Length Extension Attack | Forge a valid MAC without knowing the secret key, exploiting the length extension vulnerability of MD5/SHA-256. | [Slides](https://www.handsonsecurity.net/files/slides/C02_One_Way_Hash.pptx) | [Lab](https://seedsecuritylabs.org/Labs_20.04/Crypto/Crypto_Hash_Length_Ext/) |
| 4 | RSA Public-Key Encryption | Implement RSA algorithm from scratch: key generation, encryption, decryption, signing, verification. | [Slides](https://www.handsonsecurity.net/files/slides/C03_Public_Key_Encryption.pptx) | [Lab](https://seedsecuritylabs.org/Labs_20.04/Crypto/Crypto_RSA/) |
| 5 | Public-Key Infrastructure (PKI) | Explore PKI, digital signatures, X.509 certificates, and CA operations using OpenSSL. | [Slides](https://www.handsonsecurity.net/files/slides/C04_PKI.pptx) | [Lab](https://seedsecuritylabs.org/Labs_20.04/Crypto/Crypto_PKI/) |
| 6 | Transport Layer Security (TLS) | Write TLS client, server, and proxy programs in Python. Understand TLS handshake, certificates, and cipher suites. | [Slides](https://www.handsonsecurity.net/files/slides/C05_TLS.pptx) | [Lab](https://seedsecuritylabs.org/Labs_20.04/Crypto/Crypto_TLS/) |
| 7 | Padding Oracle Attack | Conduct padding oracle attack against a CBC-mode encryption to recover plaintext without the key. | — | [Lab](https://seedsecuritylabs.org/Labs_20.04/Crypto/Crypto_Padding_Oracle/) |
| 8 | Pseudo Random Number Generation | Generate cryptographically strong random numbers; understand the difference between `/dev/random` and `/dev/urandom`. | — | [Lab](https://seedsecuritylabs.org/Labs_20.04/Crypto/Crypto_Random_Number/) |

---

### Network Security (13 labs) — AP Unit 3

> ★★ **Moderate suitability.** ARP and TCP attack labs are engaging and visual. Requires basic networking knowledge (TCP/IP, DNS). The SEED Internet emulator makes labs safe and self-contained.

| # | Lab | Description | PPT Slides | Lab Link |
|---|---|---|---|---|
| 1 | Packet Sniffing & Spoofing | Sniff packets on the local network and spoof various types of packets using Python and C (Scapy). | [Slides](https://www.handsonsecurity.net/files/slides/N04_Sniffing_Spoofing.pptx) | [Lab](https://seedsecuritylabs.org/Labs_20.04/Networking/Sniffing_Spoofing/) |
| 2 | ARP Cache Poisoning | Launch ARP cache poisoning attacks; use it to conduct man-in-the-middle attacks. | [Slides](https://www.handsonsecurity.net/files/slides/N02_MAC_ARP.pptx) | [Lab](https://seedsecuritylabs.org/Labs_20.04/Networking/ARP_Attack/) |
| 3 | ICMP Redirect Attack | Launch ICMP redirect attacks at the IP layer to conduct man-in-the-middle attacks. | [Slides](https://www.handsonsecurity.net/files/slides/N03_IP_ICMP.pptx) | [Lab](https://seedsecuritylabs.org/Labs_20.04/Networking/ICMP_Redirect/) |
| 4 | TCP Attacks | Launch TCP session hijacking, SYN flooding, and TCP reset attacks. | [Slides](https://www.handsonsecurity.net/files/slides/N06_TCP.pptx) | [Lab](https://seedsecuritylabs.org/Labs_20.04/Networking/TCP_Attacks/) |
| 5 | The Mitnick Attack | Recreate the classic Mitnick attack — a famous real-world TCP session hijacking incident. | [Slides](https://www.handsonsecurity.net/files/slides/N06_TCP.pptx) | [Lab](https://seedsecuritylabs.org/Labs_20.04/Networking/Mitnick_Attack/) |
| 6 | DNS Attack — Local | Conduct local DNS spoofing attacks by corrupting the DNS cache on the local machine. | [Slides](https://www.handsonsecurity.net/files/slides/N10_DNS.pptx) | [Lab](https://seedsecuritylabs.org/Labs_20.04/Networking/DNS/DNS_Local/) |
| 7 | DNS Attack — Remote | Conduct remote DNS spoofing attacks by sniffing and forging DNS responses. | [Slides](https://www.handsonsecurity.net/files/slides/N10_DNS.pptx) | [Lab](https://seedsecuritylabs.org/Labs_20.04/Networking/DNS/DNS_Remote/) |
| 8 | DNS Rebinding Attack | Conduct DNS rebinding attacks to bypass browser's same-origin policy. | [Slides](https://www.handsonsecurity.net/files/slides/N10_DNS.pptx) | [Lab](https://seedsecuritylabs.org/Labs_20.04/Networking/DNS/DNS_Rebinding/) |
| 9 | DNS Infrastructure Attack | Attack the DNS infrastructure by setting up a malicious DNS server. | [Slides](https://www.handsonsecurity.net/files/slides/N10_DNS.pptx) | [Lab](https://seedsecuritylabs.org/Labs_20.04/Networking/DNS/DNS_Infrastructure/) |
| 10 | DNSSEC | Configure and test DNSSEC to defend against DNS attacks. | [Slides](https://www.handsonsecurity.net/files/slides/N11_DNSSEC.pptx) | [Lab](https://seedsecuritylabs.org/Labs_20.04/Networking/DNS/DNSSEC/) |
| 11 | Firewall Exploration | Write a simple packet-filter firewall using Python and Netfilter; experiment with Linux's built-in firewall. | [Slides](https://www.handsonsecurity.net/files/slides/N07_Firewalls.pptx) | [Lab](https://seedsecuritylabs.org/Labs_20.04/Networking/Firewall/) |
| 12 | Firewall Evasion | Bypass firewalls using static port forwarding, dynamic port forwarding (SOCKS), and VPN. | [Slides](https://www.handsonsecurity.net/files/slides/N09_Tunneling.pptx) | [Lab](https://seedsecuritylabs.org/Labs_20.04/Networking/Firewall_Evasion/) |
| 13 | VPN Tunneling | Incrementally build a simple VPN program using the TUN/TAP interface to learn how VPN tunneling works. | [Slides](https://www.handsonsecurity.net/files/slides/N08_VPN.pptx) | [Lab](https://seedsecuritylabs.org/Labs_20.04/Networking/VPN_Tunnel/) |
| 14 | VPN (Full Project) | Design and implement a mini-VPN using TUN/TAP and TLS. Requires at least a month — good for a final project. | [Slides](https://www.handsonsecurity.net/files/slides/N08_VPN.pptx) | [Lab](https://seedsecuritylabs.org/Labs_20.04/Networking/VPN/) |
| 15 | BGP Exploration & Attack | Use an Internet simulator to learn BGP, configure autonomous systems, and launch BGP attacks. | [Slides](https://www.handsonsecurity.net/files/slides/N12_BGP.pptx) | [Lab](https://seedsecuritylabs.org/Labs_20.04/Networking/BGP/BGP_Exploration_Attack/) |
| 16 | Morris Worm | Write a simple Internet worm and test it in an Internet emulator. | — | [Lab](https://seedsecuritylabs.org/Labs_20.04/Networking/Morris_Worm/) |
| 17 | Heartbleed Attack | Exploit the Heartbleed vulnerability (CVE-2014-0160) to steal secrets from a remote server. | [Slides](https://www.handsonsecurity.net/files/slides/N13_Heartbleed.pptx) | [Lab](https://seedsecuritylabs.org/Labs_20.04/Networking/Heartbleed/) |

---

### Software Security (9 labs) — AP Unit 4

> ★ **Advanced.** These labs require C programming and understanding of memory layout. Best for advanced high school students or as teacher demonstration material. The concepts (buffer overflow, privilege escalation) are directly relevant to AP Unit 4.

| # | Lab | Description | PPT Slides | Lab Link |
|---|---|---|---|---|
| 1 | Environment Variable & Set-UID | Launch attacks on privileged Set-UID root programs; understand risks of environment variables and the `system()` function. | [Slides](https://www.handsonsecurity.net/files/slides/S02_SetUID.pptx) | [Lab](https://seedsecuritylabs.org/Labs_20.04/Software/Environment_Variable_and_SetUID/) |
| 2 | Buffer Overflow (Set-UID) | Exploit buffer-overflow vulnerability in a privileged Set-UID program to gain root access. | [Slides](https://www.handsonsecurity.net/files/slides/S04_Buffer_Overflow.pptx) | [Lab](https://seedsecuritylabs.org/Labs_20.04/Software/Buffer_Overflow_Setuid/) |
| 3 | Buffer Overflow (Server) | Exploit buffer-overflow vulnerability in a server program; experiment with countermeasures (ASLR, NX, StackGuard). | [Slides](https://www.handsonsecurity.net/files/slides/S04_Buffer_Overflow.pptx) | [Lab](https://seedsecuritylabs.org/Labs_20.04/Software/Buffer_Overflow_Server/) |
| 4 | Buffer Overflow (ARM64) | Buffer overflow attack on Apple Silicon (ARM64) machines. | [Slides](https://www.handsonsecurity.net/files/slides/S04_Buffer_Overflow.pptx) | [Lab](https://seedsecuritylabs.org/Labs_20.04/Software/Buffer_Overflow_Server_ARM64/) |
| 5 | Return-to-Libc Attack | Use return-to-libc technique to defeat the non-executable stack countermeasure. (32-bit only) | [Slides](https://www.handsonsecurity.net/files/slides/S05_Return_to_Libc.pptx) | [Lab](https://seedsecuritylabs.org/Labs_20.04/Software/Return_to_Libc/) |
| 6 | Shellcode Development | Write shellcode from scratch — understand how shellcode works in buffer overflow attacks. | [Slides](https://www.handsonsecurity.net/files/slides/S09_Shellcode.pptx) | [Lab](https://seedsecuritylabs.org/Labs_20.04/Software/Shellcode/) |
| 7 | Format String Vulnerability | Exploit format string vulnerability to crash programs, steal sensitive data, and inject malicious code. | [Slides](https://www.handsonsecurity.net/files/slides/S06_Format_String.pptx) | [Lab](https://seedsecuritylabs.org/Labs_20.04/Software/Format_String/) |
| 8 | Race Condition Vulnerability | Exploit race condition vulnerability in a privileged program; experiment with countermeasures. | [Slides](https://www.handsonsecurity.net/files/slides/S07_Race_Condition.pptx) | [Lab](https://seedsecuritylabs.org/Labs_20.04/Software/Race_Condition/) |
| 9 | Dirty COW Attack | Exploit the Dirty COW race condition vulnerability (CVE-2016-5195) in the Linux kernel to gain root privilege. | [Slides](https://www.handsonsecurity.net/files/slides/S08_DirtyCOW_Attack.pptx) | [Lab](https://seedsecuritylabs.org/Labs_20.04/Software/Dirty_COW/) |

---

### System (Hardware) Security (2 labs) — AP Unit 4

> ★ **Very advanced.** Requires understanding of CPU architecture, cache memory, and assembly. Best used as teacher demonstration or for highly motivated students.

| # | Lab | Description | PPT Slides | Lab Link |
|---|---|---|---|---|
| 1 | Meltdown Attack | Exploit the Meltdown vulnerability (CVE-2017-5754) in Intel CPUs to read kernel memory from user space. | [Slides](https://www.handsonsecurity.net/files/slides/H01_MeltdownSpectre.pptx) | [Lab](https://seedsecuritylabs.org/Labs_20.04/System/Meltdown_Attack/) |
| 2 | Spectre Attack | Exploit the Spectre vulnerability (CVE-2017-5753) in Intel CPUs using branch prediction. | [Slides](https://www.handsonsecurity.net/files/slides/H01_MeltdownSpectre.pptx) | [Lab](https://seedsecuritylabs.org/Labs_20.04/System/Spectre_Attack/) |

---

### Blockchain Security (3 labs) — AP Unit 5

> ★★ **Moderate.** Uses the SEED Internet emulator. Good for students interested in cryptocurrency and smart contracts. The reentrancy attack (DAO hack) is a famous real-world case study.

| # | Lab | Description | Lab Link |
|---|---|---|---|
| 1 | Blockchain Exploration | Get familiar with blockchain basics: accounts, wallets, transactions, and blocks. Uses SEED Internet emulator. (Beta) | [Lab](https://seedsecuritylabs.org/Labs_20.04/Blockchain/Blockchain_Exploration/) |
| 2 | Smart Contract | Learn smart contract development: deployment, invocation, sending funds to/from contracts. Uses SEED Internet emulator. (Beta) | [Lab](https://seedsecuritylabs.org/Labs_20.04/Blockchain/Smart_Contract/) |
| 3 | Smart Contract Reentrancy Attack | Exploit the reentrancy vulnerability in smart contracts (the famous DAO hack). Uses SEED Internet emulator. | [Lab](https://seedsecuritylabs.org/Labs_20.04/Blockchain/Reentrancy_Attack/) |

---

### Mobile Security (2 labs) — Deprecated

> ⚠ These labs are no longer supported and will be removed. Listed for reference only.

| # | Lab | Description | Lab Link |
|---|---|---|---|
| 1 | Android Repackaging Attack | Insert malicious code inside an existing Android app and repackage it. | [Lab](https://seedsecuritylabs.org/Labs_20.04/Mobile/Android_Repackaging/) |
| 2 | Android Rooting Attack | Develop an OTA package from scratch to root an Android device. | [Lab](https://seedsecuritylabs.org/Labs_20.04/Mobile/Android_Rooting/) |

---

## Lecture Slides (PPT)

Complete slide decks for all SEED topics, freely downloadable from [handsonsecurity.net/resources](https://www.handsonsecurity.net/resources.html).

| Category | Topics | Slides |
|---|---|---|
| **Software Security** | Linux Security Basics, Set-UID, Environment Variables, Buffer Overflow, Return-to-Libc & ROP, Format String, Race Condition, Dirty COW, Shellcode | [S01–S09](https://www.handsonsecurity.net/resources.html) |
| **Web Security** | Web Security Basics, CSRF, XSS, SQL Injection, Clickjacking, Shellshock | [W01–W06](https://www.handsonsecurity.net/resources.html) |
| **Network Security** | Network Basics, MAC/ARP, IP/ICMP, Sniffing/Spoofing, UDP, TCP, DNS, DNSSEC, Firewall, VPN, Tunneling, BGP, Heartbleed, Reverse Shell | [N01–N14](https://www.handsonsecurity.net/resources.html) |
| **Cryptography** | Secret-Key Encryption, One-Way Hash, Public-Key Encryption, PKI, TLS, Bitcoin & Blockchain | [C01–C06](https://www.handsonsecurity.net/resources.html) |
| **Hardware Security** | Meltdown & Spectre | [H01](https://www.handsonsecurity.net/resources.html) |

Each topic also includes practice problems (PDF). Solution manuals are available to instructors who adopt the textbook.

---

## Video Courses (Udemy)

Prof. Du offers full video lecture courses on Udemy with discount codes:

| Course | Topics | Link |
|---|---|---|
| **Computer Security** | Software security, buffer overflow, shellcode, format string, race condition, Dirty COW, Meltdown/Spectre | [Udemy](https://www.udemy.com/course/du-computer-security/?referralCode=A22952E661213A336573&couponCode=SEED2026A0708) |
| **Internet Security** | Network security, sniffing/spoofing, ARP/TCP/DNS attacks, firewalls, VPN, BGP, Heartbleed | [Udemy](https://www.udemy.com/course/du-internet-security/?referralCode=9279DCD7BAFFAC610D6B&couponCode=SEED2026A0708) |
| **Web Security** | XSS, CSRF, SQL injection, clickjacking, Shellshock | [Udemy](https://www.udemy.com/course/web-security-du/?referralCode=E6E591AF1BE86914BBA6&couponCode=SEED2026A0708) |
| **Cryptography** | Secret-key encryption, hash functions, RSA, PKI, TLS, blockchain | [Udemy](https://www.udemy.com/course/du-cryptography/?referralCode=D1011CAA63DD07F8A392&couponCode=SEED2026A0708) |

> Use coupon code `SEED2026A0708` for a discount.

---

## Chinese Textbook

### 《计算机安全导论：深度实践》

| Item | Details |
|---|---|
| **Author** | 杜文亮 (Prof. Wenliang Du) |
| **Publisher** | 高等教育出版社 (April 2020) |
| **ISBN** | 9787040538823 |
| **Page** | [handsonsecurity.net/chinese](https://www.handsonsecurity.net/chinese/index.html) |
| **Purchase** | [天猫](https://detail.tmall.com/item.htm?id=618960994919) / [京东](https://item.jd.com/12649517.html) / [当当网](http://product.dangdang.com/28541420.html) |

**Content highlights:**
- Covers application security, web security, and network security
- Every theory chapter is paired with SEED hands-on labs
- Emphasizes building a knowledge system — connecting related concepts (e.g., all injection attacks share a root cause)
- Deep technical detail: buffer overflow gets two full chapters, from memory layout to attack to defense to bypassing defenses

**Sample chapters:**
- [目录 (Table of Contents)](https://www.handsonsecurity.net/files/chapters/toc_chinese.pdf)
- [前言 (Preface)](https://www.handsonsecurity.net/files/chapters/preface_chinese.pdf)
- [第4章 缓冲区溢出攻击 (Buffer Overflow)](https://www.handsonsecurity.net/files/chapters/buffer_overflow_c.pdf)
- [第13章 对 TCP 的攻击 (TCP Attacks)](https://www.handsonsecurity.net/files/chapters/tcp_attacks_c.pdf)

---

## SEED Labs → AP Cybersecurity Unit Mapping

| AP Unit | SEED Categories | Recommended Starting Labs |
|---|---|---|
| **Unit 1: Introduction to Security** | — (general concepts) | Use PPT slides for overview lectures; no specific SEED lab needed |
| **Unit 2: Securing Spaces** | — (physical security) | SEED does not cover physical security |
| **Unit 3: Securing Networks** | Network Security (13 labs) | Start with: Packet Sniffing → ARP Attack → TCP Attacks → Firewall |
| **Unit 4: Securing Devices** | Software Security (9 labs), System Security (2 labs) | Start with: Environment Variable & Set-UID → Buffer Overflow (concept via PPT) |
| **Unit 5: Securing Applications and Data** | Web Security (5 labs), Cryptography (8 labs), Blockchain (3 labs) | Start with: XSS → SQL Injection → Secret-Key Encryption → RSA → PKI |

---

## Middle School Adaptation Guide

### Recommended Approach

1. **Start with PPT slides** — Use the lecture slides to teach concepts before any hands-on lab. Slides are well-structured and include practice problems.
2. **Web Security labs first** — XSS, CSRF, and SQL injection are the most accessible. They use pre-built vulnerable apps (Elgg, Cupcakes) and require minimal prerequisites.
3. **Cryptography concepts via PPT + CyberChef** — Teach encryption/hashing concepts with slides, then use [CyberChef](https://cyberchef.org/) for hands-on exploration before attempting full SEED crypto labs.
4. **Network basics with visual tools** — Use the sniffing/spoofing lab as a demonstration. The SEED Internet emulator provides a safe, contained environment.
5. **Software Security as teacher demo** — Buffer overflow is a great concept to demonstrate, but having students complete the full lab requires C programming skills.

### Labs to Skip for Middle School

- Return-to-Libc, Shellcode Development (too advanced)
- Meltdown, Spectre (require deep CPU architecture knowledge)
- VPN full project (month-long, too complex)
- BGP, Morris Worm (require advanced networking knowledge)
- Mobile Security labs (deprecated)

### Suggested Mini-Course (8 sessions)

| Session | Topic | Activity |
|---|---|---|
| 1 | Web Security Basics | PPT: W01 Web Security Basics + practice problems |
| 2 | XSS Attack | PPT: W03 + SEED XSS Lab (simplified) |
| 3 | SQL Injection | PPT: W04 + SEED SQL Injection Lab |
| 4 | CSRF Attack | PPT: W02 + SEED CSRF Lab |
| 5 | Cryptography Basics | PPT: C01 + CyberChef hands-on |
| 6 | Hash Functions | PPT: C02 + MD5 Collision Lab (demonstration) |
| 7 | Public-Key Encryption | PPT: C03 + RSA Lab (simplified) |
| 8 | Network Security Basics | PPT: N01 + Packet Sniffing Lab (demonstration) |
