# ⚙️ GG3 Infrastructure · `gg3-dev`

This is the home of Juan Garcia's professional infrastructure stack, managed under the `gg3-dev` namespace.  
It contains internal tools, documentation, configuration standards, and reusable automation scripts that power the GG3 Lab and Oak Root Collective.

---

## 🧱 What's Inside

| Directory / Repo         | Purpose                                                                                  |
|--------------------------|------------------------------------------------------------------------------------------|
| `gg3-docs`               | Homelab & infrastructure documentation (public)                                         |
| `gg3utils`               | Shared Python tools for DevOps & system automation                                      |
| `.gg3.conf` (Private)     | Private dotfiles repo for internal system setup (configs, SSH settings, etc.) |
| *(Coming soon)*          | Jenkins pipeline scripts, Ansible roles, dotfiles bootstrap                            |

---

## 🧰 Tech Stack

### 🖥️ Hypervisor & Virtualization
- **XCP-ng**: Open-source hypervisor for all production VMs
- **Xen Orchestra (XOA)**: Self-hosted web UI to manage VM lifecycle, snapshots, and metrics

### 🌐 Web & Proxy Services
- **NGINX**: Reverse proxy, static site hosting, and HTTPS termination
- **Certbot + Let's Encrypt**: Automated TLS certificate issuance using DNS-01 validation

### 🔐 Access & Security
- **SSH**: Key-based authentication with host isolation and role separation
- **Tailscale**: Temporary remote access while WireGuard and pfSense are in development
- **Custom SSH Config**: Separated `.gg3.conf` for internal-only environments

### 🔄 Automation & DevOps
- **Jenkins**: Triggered jobs for VM snapshots, future CI/CD workflows
- **Python (gg3utils)**: Home-grown scripts for deployment, backups, and file sync
- **Future**: Ansible-based provisioning and infrastructure-as-code

### 🗄️ File Services
- **Samba (SMB)**: Internal file sharing across devices (Mac, Linux, iPad)
- **vsftpd (Deprecated)**: Initially used, now fully removed
- **SFTP (OpenSSH)**: Secure replacement with user-chrooted access planned

---

## 👤 Identity & Scope

This organization supports infrastructure managed by:

- **Juan Garcia** (`@0xjuang`)
- Operator handle: `0x1G`
- Project alias: **GG3 Lab**
- Org: **Oak Root Collective**

This is the backend environment supporting scripting, experimentation, DevOps learning, and secure growth.

---

## 🔐 Private Infrastructure Philosophy

All public-facing code and docs here are:

- Redacted for privacy (see: `gg3-sanitization-guide.md`)
- Meant for demonstration, education, and future automation reuse
- Managed intentionally with reproducibility, security, and clarity in mind

Security is prioritized from naming convention to key isolation to TLS policy.

---

## 🌐 Related Public Profiles

- GitHub (public persona): [github.com/0xjuang](https://github.com/0xjuang)
- Website: [info.gg3.dev](https://info.gg3.dev)
- Core Org: [Oak Root Collective](https://oak-root.dev) *(coming soon)*

---

_Curated under the GG3 Infrastructure Stack – designed for reproducibility, auditability, and clarity._

