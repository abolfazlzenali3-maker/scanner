# Scanner

[![CI](https://github.com/abolfazlzenali3-maker/scanner/actions/workflows/ci.yml/badge.svg)](https://github.com/abolfazlzenali3-maker/scanner/actions/workflows/ci.yml)

> Python-based **web pentest recon & vulnerability scanner** for Kali Linux —
> 30 modules, cyber UI, ranked findings, and JSON reports written at runtime.

```text
┌──(kali㉿kali)-[~/scanner]
└─$ ./scanner.py --help
usage: scanner.py [-h] [--all] [--turbo] [--tor] [--proxy PROXY] [target]
```

![Python](https://img.shields.io/badge/Python-3-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Kali Linux](https://img.shields.io/badge/Kali%20Linux-557C94?style=for-the-badge&logo=kalilinux&logoColor=white)
![Creator](https://img.shields.io/badge/Creator-abolfazlzenali-00ff41?style=for-the-badge)
![Scope](https://img.shields.io/badge/Scope-Authorized%20labs%20only-00ff41?style=for-the-badge)

## Overview

Scanner is a self-contained Python security tool for **authorized web
application penetration testing**. It performs fast recon and lightweight
vulnerability probing across **OWASP Top 10**-style classes: SQL injection,
XSS, SSRF, LFI / path traversal, CORS misconfiguration, open redirect,
host-header injection, sensitive file exposure and more.

Built and tested on **Kali Linux**, with **Burp Suite** / **OWASP ZAP**
workflows in mind. Findings are ranked (CRITICAL → INFO) and saved as a fresh
`scan_<host>_<timestamp>.json` report after every run.

```text
target → recon → probes → ranked findings → scan_<host>_<timestamp>.json
```

**GitHub topics:** `cybersecurity` · `python` · `pentesting` · `recon` ·
`kali-linux` · `vulnerability-scanner` · `web-pentest` · `owasp` ·
`bug-bounty` · `security-tools` · `infosec` · `network-recon`

## Use cases

- Authorized **web app pentesting** and **bug bounty** recon
- Quick **OWASP Top 10** surface checks before manual testing with Burp Suite / ZAP
- **Python automation** for repetitive recon tasks in Kali Linux
- Lab practice on targets you own, such as **DVWA** or local web apps

## Download

```bash
git clone https://github.com/abolfazlzenali3-maker/scanner.git
cd scanner
```

Or on GitHub, click the green **Code** button → **Download ZIP**, then
extract the folder and open a terminal inside it.

## How to run

```bash
# Show all options
python3 scanner.py --help

# Run every module against a target
python3 scanner.py example.com --all

# Fast recon profile
python3 scanner.py example.com --turbo

# Route traffic through Tor (socks5h://127.0.0.1:9050)
python3 scanner.py example.com --tor

# Or use the launcher
./run.sh example.com --all
```

You will be asked for a target if you run it without one:

```bash
python3 scanner.py
```

## Files

| File | Description |
| :--- | :--- |
| `scanner.py` | Main self-contained Python script |
| `README.md` | This description |
| `run.sh` | Launcher script |
| `requirements.txt` | Required external tools |
| `docs/OWASP-MAPPING.md` | Module-to-OWASP category mapping |
| `LICENSE` | MIT license |

Reports are **not stored in this repository**. Each run writes a fresh
`scan_<host>_<timestamp>.json` file into the directory where you run it.

## OWASP coverage

See [`docs/OWASP-MAPPING.md`](docs/OWASP-MAPPING.md) for a practical mapping
between the scanner modules and OWASP Top 10 categories. These are heuristic
checks only — always confirm findings manually.

## Requirements

Kali Linux already includes most of them. Otherwise install from
`requirements.txt`: `python3`, `curl`, `dnsutils`, `whois`, `tor`.

## Creator

**abolfazlzenali** — [GitHub profile](https://github.com/abolfazlzenali3-maker)

## Note

Authorized security testing only. Do not scan systems you do not own or
have explicit permission to test.
