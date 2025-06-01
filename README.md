# DevSecOps Infrastructure · GG3-DevNet

_Automated systems. Hardened configs. Terminal-native tooling._

![Python](https://img.shields.io/badge/Python-3670A0?style=for-the-badge&logo=python&logoColor=ffffff)
![Bash](https://img.shields.io/badge/Bash-121011?style=for-the-badge&logo=gnubash&logoColor=white)
![Puppet](https://img.shields.io/badge/Puppet-302B6D?style=for-the-badge&logo=puppet&logoColor=yellow)
![NGINX](https://img.shields.io/badge/Nginx-009639?style=for-the-badge&logo=nginx&logoColor=white)
![XCP-ng](https://img.shields.io/badge/XCP--ng-003399.svg?style=for-the-badge&logo=rocket&logoColor=white)
![Tailscale](https://img.shields.io/badge/Tailscale-242424.svg?style=for-the-badge&logo=Tailscale&logoColor=white)
![Debian](https://img.shields.io/badge/Debian-A81D33.svg?style=for-the-badge&logo=Debian&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624.svg?style=for-the-badge&logo=linux&logoColor=black)
![Zsh](https://img.shields.io/badge/Zsh-F15A24.svg?style=for-the-badge&logo=Zsh&logoColor=white)
![Vim](https://img.shields.io/badge/Vim-019733.svg?style=for-the-badge&logo=Vim&logoColor=white)
![tmux](https://img.shields.io/badge/tmux-1BB91F.svg?style=for-the-badge&logo=tmux&logoColor=white)
![Markdown](https://img.shields.io/badge/Markdown-000000.svg?style=for-the-badge&logo=Markdown&logoColor=white)

---

## 🧰 What's Inside

This GitHub organization contains the actual infrastructure stack powering GG3-DevNet — a homelab-based environment for DevOps, security, and system engineering practice. Everything here is tested in production-like conditions with a focus on auditability, reproducibility, and secure defaults.

```sh
~/gg3-dev
├── gg3-docs         # system architecture, firewall policies, SSH setup
├── gg3utils         # network tools, port scanners, UFW checkers (Python/Bash)
├── gg3-admin-tools  # bootstrap scripts, SSH key management, dotfiles deploy
├── puppet-modules   # config management for Debian servers (in progress)
└── .gg3.conf        # internal-only: shell config, install scripts, redacted from public
```

---

## 🔧 Infra Components

- **XCP-ng** — Bare-metal hypervisor w/ static IP segmentation and manual snapshot control  
- **Puppet** — WIP modules for enforcing packages, user config, and service states  
- **NGINX** — Hardened TLS web proxy and Certbot-enabled static site hosting  
- **UFW** — Host-level firewalls locked to key-based SSH only  
- **Tailscale** — Temporary fallback access until WireGuard is deployed  
- **Bash & Python** — Health checks, audits, and provisioning tools run entirely in terminal

---

## 🔐 DevSecOps Practices

```sh
# Scan critical range
nmap -sS 10.0.0.0/24

# Check UFW and verify port lock
sudo ufw status verbose

# Deploy internal config
sudo ./deploy.sh --env dev
```

- SSH key auth only — namespaced by function and host  
- Firewalls deny all except pre-approved ports  
- TLS enforced with manual NGINX hardening  
- Dotfiles tracked and deployed like code  
- All config changes documented in plaintext and Markdown

---

## 📂 Active Projects

| Repo                | Role                                                             |
|---------------------|------------------------------------------------------------------|
| `gg3-docs`          | Lab architecture, config standards, SSH key layout               |
| `gg3utils`          | Terminal-native tooling for audits, scans, and monitoring        |
| `gg3-admin-tools`   | ZSH/bootstrap automation, SSH key rotation, deploy helpers       |
| `puppet-modules`    | Declarative state management (packages, users, services)         |

---

## 🧑‍💻 Maintainer

Juan Garcia — `@0x1G` / [`0xjuang`](https://github.com/0xjuang)  
- Email: [juan@gg3.dev](mailto:juan@gg3.dev)  
- Site: [about.gg3.dev](https://about.gg3.dev)  
- LinkedIn: [linkedin.com/in/0xjuang](https://linkedin.com/in/0xjuang)

---

## 🔐 Notes on Privacy & Structure

- No internal IPs, DNS names, or secrets are exposed  
- All tools are used actively — nothing speculative or aspirational  
- Designed to be portable across Debian systems and lab-scale deployments  

> Infrastructure shouldn’t lie. What’s here reflects what’s running.

---

_Last updated: June 2025 · Signed: 0x1G_
