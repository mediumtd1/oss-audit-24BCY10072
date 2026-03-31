<div align="center">

<br/>

```
 ██████╗ ███████╗███████╗     █████╗ ██╗   ██╗██████╗ ██╗████████╗
██╔═══██╗██╔════╝██╔════╝    ██╔══██╗██║   ██║██╔══██╗██║╚══██╔══╝
██║   ██║███████╗███████╗    ███████║██║   ██║██║  ██║██║   ██║   
██║   ██║╚════██║╚════██║    ██╔══██║██║   ██║██║  ██║██║   ██║   
╚██████╔╝███████║███████║    ██║  ██║╚██████╔╝██████╔╝██║   ██║   
 ╚═════╝ ╚══════╝╚══════╝    ╚═╝  ╚═╝ ╚═════╝ ╚═════╝ ╚═╝   ╚═╝  
```

# 🔍 The Open Source Audit — Git

### A Capstone Project for the Open Source Software (OSS NGMC) Course

[![License: GPL v2](https://img.shields.io/badge/License-GPL%20v2-blue.svg)](https://www.gnu.org/licenses/old-licenses/gpl-2.0.html)
[![Subject](https://img.shields.io/badge/Subject-Open%20Source%20Software-teal.svg)]()
[![VIT](https://img.shields.io/badge/Institution-VIT%20Bhopal-navy.svg)]()
[![Unit Coverage](https://img.shields.io/badge/Units-1--5-orange.svg)]()
[![Max Marks](https://img.shields.io/badge/Max%20Marks-100-green.svg)]()

<br/>

> *"Every time I type `git push`, I am participating in a legacy of independence that was bought through the BitKeeper crisis."*

<br/>

</div>

---

## 👤 Student Details

| Field | Details |
|-------|---------|
| **Name** | Prateek Mishra |
| **Registration No.** | 24BCY10072 |
| **Slot** | F11 |
| **Date of Submission** | 31 March 2026 |
| **Course** | Open Source Software — NGMC |
| **Max Marks** | 100 |

---

## 📖 Project Overview

This repository contains my **Capstone Project** for the Open Source Software course at VIT Bhopal. Rather than just *using* open-source tools, this project is a deep, structured **audit** of one of the most foundational tools in software engineering — **Git**.

The audit is split into two phases:

- **Philosophical Investigation** — Tracing Git's origin from the 2005 BitKeeper crisis, dissecting the GNU GPL v2 license, and examining the ethics of the FOSS movement.
- **Technical Footprint** — Installing Git on Ubuntu 24.04.3 LTS (WSL2), mapping its filesystem layout, and writing five practical Bash automation scripts.

The goal is not just academic compliance — it is to understand *why* Git exists, *how* it is protected by law, and *what* it means to be an ethical engineer in a world built on open-source foundations.

---

## 📚 Table of Contents

1. [Project Structure](#-project-structure)
2. [Part A — Origin and Philosophy](#-part-a--origin-and-philosophy)
3. [Part B — Linux Footprint](#-part-b--linux-footprint)
4. [Part C — The FOSS Ecosystem](#-part-c--the-foss-ecosystem)
5. [Part D — Open Source vs Proprietary](#-part-d--open-source-vs-proprietary)
6. [Shell Scripts](#-shell-scripts)
7. [Installation & Setup](#-installation--setup)
8. [Screenshots](#-screenshots)
9. [License](#-license)

---

## 📁 Project Structure

```
oss-audit-24BCY10072/
│
├── README.md                         ← You are here
│
├── report/
│   └── OSSCapstoneProject.docx       ← Full formal report (14 pages)
│
├── scripts/
│   ├── 01_system_identity.sh         ← Script 1: System Identity Report
│   ├── 02_foss_package_inspector.sh  ← Script 2: FOSS Package Inspector
│   ├── 03_disk_permission_auditor.sh ← Script 3: Disk & Permission Auditor
│   ├── 04_log_file_analyser.sh       ← Script 4: Log File Analyser
│   └── 05_manifesto_generator.sh     ← Script 5: Open Source Manifesto Generator
│
└── screenshots/
    ├── system_identity.png
    ├── foss_inspector.png
    ├── disk_auditor.png
    ├── log_analyser.png
    └── manifesto_generator.png
```

---

## 🧠 Part A — Origin and Philosophy

### The BitKeeper Crisis (2005)

By the early 2000s, the Linux kernel was managed using **BitKeeper** — a proprietary tool. When developer Andrew Tridgell attempted to reverse-engineer a free client for it, BitMover revoked the free license for the entire Linux community **overnight**.

This single event forced Linus Torvalds to build a replacement in **two weeks** — and Git was born.

### Why Git Was Radical

| Requirement | What It Meant |
|-------------|--------------|
| **Speed** | Apply a patch in under one second |
| **Distributed** | Every developer holds the full history |
| **Integrity** | Every file hashed via SHA-1 |

### The GNU GPL v2 — Four Freedoms

```
Freedom 0 → Run the program for any purpose
Freedom 1 → Study and modify the source code
Freedom 2 → Redistribute copies to others
Freedom 3 → Distribute your modified versions
```

The GPL v2's **Copyleft** mechanism ensures that any derivative work must remain open. It turns copyright law on its head — using it to *guarantee* freedom rather than restrict it.

---

## 🐧 Part B — Linux Footprint

### Environment

- **OS:** Ubuntu 24.04.3 LTS (WSL2 on Windows)
- **Kernel:** Verified via `uname -a`
- **Installation:** `sudo apt update && sudo apt install git -y`

### Key Filesystem Locations

```bash
/usr/bin/git          # The Git executable binary
/etc/gitconfig        # System-wide configuration
~/.gitconfig          # Per-user configuration (name, email)
/usr/share/doc/git    # Man pages and offline documentation
```

### Security Design

Git runs under **local user privileges** — following the **Principle of Least Privilege**. It is a transient utility, not a persistent daemon, meaning it consumes no resources when idle.

### Patch Management Pipeline

```
Vulnerability Found
       ↓
Git Maintainers Release Fix (upstream)
       ↓
Ubuntu Security Team Backports It
       ↓
Your Machine Gets It via: sudo apt upgrade
```

---

## 🌐 Part C — The FOSS Ecosystem

### Core Dependencies

| Library | Role |
|---------|------|
| `zlib` | Data compression of repository objects |
| `libcurl` | Internet communication (`git clone`, `git push`) |
| `OpenSSL` | Encrypted, secure connections to remotes |

### Governance

Git is maintained by **Junio Hamano** and a global community. All decisions are made via public **mailing lists** — fully searchable and transparent. No single company controls the roadmap.

### The Git Effect

Git enabled the entire **DevOps ecosystem** — Jenkins, Docker, Kubernetes, GitHub, GitLab all use Git as their source of truth. Without its decentralised design, the modern cloud would be slower and far more proprietary.

---

## ⚖️ Part D — Open Source vs Proprietary

### Git vs Perforce (Helix Core)

| Dimension | Git (Open Source) | Perforce (Proprietary) |
|-----------|-------------------|------------------------|
| **Cost** | Free for everyone | Per-user subscription fees |
| **Security** | Public audit — anyone can inspect source | Black box — vendor-only access |
| **Support** | Community forums, Stack Overflow, docs | Corporate SLA, dedicated team |
| **Freedom** | Full — modify and redistribute under GPL v2 | Restricted — no source access |
| **Control** | Community governed | Single company controls roadmap |

### Verdict

> Git is recommended for virtually every real-world software deployment. Its speed, distributed nature, and permanent community governance make it the most future-proof choice for any professional engineer.

---

## 🖥️ Shell Scripts

Five Bash scripts were developed as part of the technical audit. Each demonstrates a distinct set of shell scripting competencies.

### Script 1 — System Identity Report
```bash
bash scripts/01_system_identity.sh
```
Displays kernel version, OS info, uptime, and a GPL license note using command substitution.

**Concepts:** Variables · `echo` · Command substitution `$(...)` · Output formatting

---

### Script 2 — FOSS Package Inspector
```bash
bash scripts/02_foss_package_inspector.sh
```
Checks if Git is installed via `dpkg -s`. Uses a `case` statement to output a philosophical description of the tool.

**Concepts:** `if-then-else` · `case` statements · `dpkg` · `grep`

---

### Script 3 — Disk & Permission Auditor
```bash
bash scripts/03_disk_permission_auditor.sh
```
Iterates through critical directories (`/etc`, `/var/log`, etc.) and reports permissions and disk usage.

**Concepts:** `for` loops · `[ -d ]` checks · `awk` / `cut` text processing

---

### Script 4 — Log File Analyser
```bash
bash scripts/04_log_file_analyser.sh <logfile> <keyword>
```
Processes a log file line-by-line and counts keyword occurrences (e.g., `error`, `warning`).

**Concepts:** `while read` loops · Counter arithmetic `$((...))` · CLI arguments `$1`

---

### Script 5 — Open Source Manifesto Generator
```bash
bash scripts/05_manifesto_generator.sh
```
Interactively asks the user about their FOSS values and writes a personalised manifesto to a `.txt` file.

**Concepts:** `read` · String concatenation · Output redirection `>`

---

## ⚙️ Installation & Setup

To explore and run the shell scripts on your own Linux or WSL2 system:

### 1. Clone the repository
```bash
git clone https://github.com/Prateek-Mishra-24BCY10072/oss-audit-24BCY10072.git
cd oss-audit-24BCY10072
```

### 2. Make scripts executable
```bash
chmod +x scripts/*.sh
```

### 3. Verify Git is installed
```bash
git --version
# Expected: git version 2.x.x
```

### 4. Run any script
```bash
bash scripts/01_system_identity.sh
```

### Prerequisites

- Ubuntu 20.04+ / Debian-based Linux (or WSL2 on Windows)
- `git` installed via `sudo apt install git -y`
- Bash 5.0+

---

## 📸 Screenshots

### System Identity Report
![System Identity](screenshots/system_identity.png)

### FOSS Package Inspector
![FOSS Inspector](screenshots/foss_inspector.png)

### Disk & Permission Auditor
![Disk Auditor](screenshots/disk_auditor.png)

### Log File Analyser
![Log Analyser](screenshots/log_analyser.png)

### Open Source Manifesto Generator
![Manifesto Generator](screenshots/manifesto_generator.png)

---

## 📄 License

This project is submitted as academic coursework under VIT Bhopal's Open Source Software course.

The subject of this audit — **Git** — is licensed under the **GNU General Public License v2.0**.

[![License: GPL v2](https://img.shields.io/badge/License-GPL%20v2-blue.svg)](https://www.gnu.org/licenses/old-licenses/gpl-2.0.html)

```
GNU GENERAL PUBLIC LICENSE
Version 2, June 1991

The GNU GPL v2 grants you:
  → Freedom to run the program for any purpose
  → Freedom to study and modify the source code  
  → Freedom to redistribute copies
  → Freedom to distribute your modified versions

Any derivative work must be distributed under the same license.
This ensures Git can never be "closed" or privatised.
```

For the full license text, see: https://www.gnu.org/licenses/old-licenses/gpl-2.0.html

---

<div align="center">

<br/>

**Prateek Mishra** · `24BCY10072` · Slot F11 · VIT Bhopal

*"The fact that I can download world-class tools on my laptop without a subscription fee is a privilege built on decades of open collaboration. This audit is my attempt to honour that."*

<br/>

⭐ If you found this audit useful, consider starring the repository!

</div>
