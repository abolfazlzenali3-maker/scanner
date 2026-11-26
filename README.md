# Scanner

> Advanced terminal recon / vulnerability scanner — 30 modules, cyber UI, ranked findings and JSON reporting.

```text
┌──(kali㉿kali)-[~/scanner]
└─$ ./scanner.py --help
usage: scanner.py [-h] [--all] [--turbo] [--tor] [--proxy PROXY] [target]
```

![Python](https://img.shields.io/badge/Python-3-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Kali Linux](https://img.shields.io/badge/Kali%20Linux-557C94?style=for-the-badge&logo=kalilinux&logoColor=white)
![Creator](https://img.shields.io/badge/Creator-abolfazlzenali-00ff41?style=for-the-badge)
![Scope](https://img.shields.io/badge/Scope-Authorized%20labs%20only-00ff41?style=for-the-badge)

## Files

| File | Description |
| :--- | :--- |
| `scanner.py` | Main self-contained Python script |
| `README.md` | This description |
| `run.sh` | Launcher: `./run.sh <target> [options]` |
| `requirements.txt` | Required external tools |
| `scan_*.json` | Example scan reports |

## Features

Target profile, DNS, reverse DNS, WHOIS, TCP ports, service fingerprint,
HTTP headers, TLS/SSL, robots/sitemap, directory enum, sensitive files,
backup discovery, CORS, HTTP methods, cookies, technologies, open redirect,
XSS/SQLi/LFI/SSRF probes, host header, HSTS, mixed content, admin panels,
TRACE, directory listing, Git exposure, risk score and JSON report.

## Usage

```bash
python3 scanner.py --help
python3 scanner.py example.com --all
python3 scanner.py example.com --turbo
python3 scanner.py example.com --tor
./run.sh example.com --all
```

## Requirements

See `requirements.txt`: `python3`, `curl`, `dnsutils`, `whois`, `tor`.

## Creator

**abolfazlzenali**

## Note

Authorized security testing only. Do not scan systems you do not own or
have explicit permission to test.
