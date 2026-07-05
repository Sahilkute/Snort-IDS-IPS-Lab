# Snort-IDS-IPS-Lab

# 🔍 Snort IDS/IPS Home Lab

![Snort](https://img.shields.io/badge/Snort-IDS%2FIPS-red?style=for-the-badge)
![Platform](https://img.shields.io/badge/Platform-Windows%2010%20%7C%20Ubuntu-green?style=for-the-badge)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen?style=for-the-badge)
![Blue Team](https://img.shields.io/badge/Team-Blue%20Team-blue?style=for-the-badge)

A hands-on IDS/IPS home lab built with **Snort**, configured in both Intrusion Detection and Intrusion Prevention modes — with custom rules written and tested by simulating real attacks.

---

## 🖥️ Lab Architecture

| Component | Role | OS |
|-----------|------|----|
| Snort (IDS Mode) | Passive traffic monitoring & alerting | Ubuntu |
| Snort (IPS Mode) | Inline traffic blocking & prevention | Ubuntu |
| Target Machine 1 | Monitored Endpoint | Windows 10 |
| Target Machine 2 | Monitored Endpoint | Ubuntu Desktop |
| Attacker Machine | Attack simulation | Kali Linux |

---

## ✅ Implemented Modules

### 1. 🛡️ Snort as IDS (Intrusion Detection System)
- Configured in passive/listening mode
- Monitors network traffic without blocking
- Generates alerts on suspicious activity
- 📄 [IDS Setup Documentation](docs/setup.txt)

---

### 2. 🚫 Snort as IPS (Intrusion Prevention System)
- Configured in inline mode
- Actively blocks malicious traffic in real time
- Uses iptables/NFQ for packet interception
- 📄 [IPS Setup Documentation](docs/setup.txt)

---

### 3. 📝 Custom Rule Writing & Testing
- Written custom Snort rules for real attack scenarios
- Tested rules by simulating live attacks on lab machines
- Rules mapped to common attack techniques
- 📄 [Rule Writing Documentation](docs/rule-writing.txt)

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
    ├── setup.txt           # IDS IPS setup guide
    └── rule-writing.txt        # Rule writing guide
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
| Windows 10 | Target endpoint |
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
<img width="1920" height="1080" alt="snort ss 1" src="https://github.com/user-attachments/assets/94388957-7b90-4d10-8eb4-b5f96ccb5645" />
<img width="1907" height="1072" alt="snort ss2" src="https://github.com/user-attachments/assets/a6c5c8cc-4397-44ba-b4de-a35c0241df37" />

---

## 📚 References

- [Snort Official Documentation](https://www.snort.org/documents)
- [Snort Rule Writing Guide](https://docs.snort.org/rules/)
- [MITRE ATT&CK Framework](https://attack.mitre.org/)

---

## 👤 Author

**Your Name**
- 🔗 [LinkedIn](https://linkedin.com/in/sahil-kute)
- 🐙 [GitHub](https://github.com/Sahilkute)

---

## 📜 License

This project is for educational purposes only. Use responsibly.

---

> ⭐ If you found this helpful, consider giving it a star!
