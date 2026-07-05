# Snort-IDS-IPS-Lab

# 🔍 Snort IDS/IPS Home Lab

![Snort](https://img.shields.io/badge/Snort-IDS%2FIPS-red?style=for-the-badge)
![Platform](https://img.shields.io/badge/Platform-Windows%2011%20%7C%20Ubuntu-green?style=for-the-badge)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen?style=for-the-badge)
![Blue Team](https://img.shields.io/badge/Team-Blue%20Team-blue?style=for-the-badge)

A hands-on IDS/IPS home lab built with **Snort**, configured in both Intrusion Detection and Intrusion Prevention modes — with custom rules written and tested by simulating real attacks.

---

## 🖥️ Lab Architecture

| Component | Role | OS |
|-----------|------|----|
| Snort (IDS Mode) | Passive traffic monitoring & alerting | Ubuntu |
| Snort (IPS Mode) | Inline traffic blocking & prevention | Ubuntu |
| Target Machine 1 | Monitored Endpoint | Windows 11 |
| Target Machine 2 | Monitored Endpoint | Ubuntu Desktop |
| Attacker Machine | Attack simulation | Kali Linux |

---

## ✅ Implemented Modules

### 1. 🛡️ Snort as IDS (Intrusion Detection System)
- Configured in passive/listening mode
- Monitors network traffic without blocking
- Generates alerts on suspicious activity
- 📄 [IDS Setup Documentation](docs/ids-setup.md)

---

### 2. 🚫 Snort as IPS (Intrusion Prevention System)
- Configured in inline mode
- Actively blocks malicious traffic in real time
- Uses iptables/NFQ for packet interception
- 📄 [IPS Setup Documentation](docs/ips-setup.md)

---

### 3. 📝 Custom Rule Writing & Testing
- Written custom Snort rules for real attack scenarios
- Tested rules by simulating live attacks on lab machines
- Rules mapped to common attack techniques
- 📄 [Rule Writing Documentation](docs/rule-writing.md)

---

## 📁 Repository Structure

```
Snort-IDS-IPS-Lab/
│
├── README.md
├── configs/
│   ├── snort-ids.conf         # Snort IDS configuration
│   └── snort-ips.conf         # Snort IPS configuration
├── rules/
│   └── custom.rules           # Custom detection rules
└── docs/
    ├── ids-setup.md           # IDS setup guide
    ├── ips-setup.md           # IPS setup guide
    └── rule-writing.md        # Rule writing guide
```

---

## 🚀 Getting Started

### Prerequisites
- Ubuntu machine (Snort host)
- Snort 2.x or 3.x installed
- iptables configured (for IPS mode)
- Network interface in promiscuous mode (for IDS mode)

### Install Snort
```bash
# Update packages
sudo apt-get update

# Install Snort
sudo apt-get install snort -y

# Verify installation
snort --version
```

---

## 🛠️ Tools & Technologies

| Tool | Purpose |
|------|---------|
| Snort | IDS/IPS Engine |
| iptables / NFQ | Packet interception for IPS mode |
| Kali Linux | Attack simulation |
| Windows 11 | Target endpoint |
| Ubuntu Desktop | Target endpoint |

---

## 📝 Custom Rules Highlights

| Rule | Detects | SID |
|------|---------|-----|
| ICMP Flood Detection | Ping flood / DoS | 1000001 |
| Nmap Port Scan | Reconnaissance | 1000002 |
| SSH Brute Force | Auth attack | 1000003 |
| Reverse Shell Attempt | C2 / Backdoor | 1000004 |
| SQL Injection Attempt | Web attack | 1000005 |

---

## 📸 Screenshots

> Screenshots of Snort alerts and rule testing are available in the [`screenshots/`](screenshots/) folder.

---

## 📚 References

- [Snort Official Documentation](https://www.snort.org/documents)
- [Snort Rule Writing Guide](https://docs.snort.org/rules/)
- [MITRE ATT&CK Framework](https://attack.mitre.org/)

---

## 👤 Author

**Your Name**
- 🔗 [LinkedIn](https://linkedin.com/in/yourprofile)
- 🐙 [GitHub](https://github.com/yourusername)

---

## 📜 License

This project is for educational purposes only. Use responsibly.

---

> ⭐ If you found this helpful, consider giving it a star!
