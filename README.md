# Training Simulation System (Hardened)

## Overview

This is a fully offline-capable, airgapped-ready, hardened training simulation system designed for paramilitary-grade security. It features modular architecture, secure CI/CD, automated deployment, and tamper-resistant configuration.

---

## Features

- 🛡️ Military-grade hardened security
- 🚫 No reliance on third-party services or cloud APIs
- 🔒 Full offline operation with vendored packages
- 🔁 Self-contained CI/CD with Drone CI (local)
- 🧪 Automated unit testing with pytest
- 📦 Secure package and dependency management
- 🔐 GPG + SSH-based secrets handling
- 🧰 Systemd deployment
- 📊 Real-time local monitoring via Netdata
- 🗂️ Offline documentation browser included

---

## Setup Instructions

### 1. Clone the repository (local Git server preferred)
```bash
git clone git@your-local-git-server:paracryptid/training_simulation_system.git
cd training_simulation_system
```

### 2. Install dependencies from local cache
```bash
pip install --no-index --find-links=packages -r requirements.txt
```

### 3. Run tests
```bash
pytest
```

### 4. Start system with systemd
```bash
sudo systemctl start simulation.service
```

---

## Secrets & Configuration

- Secrets stored in `secrets/.env.gpg` (encrypted with GPG)
- Load environment with `source <(gpg --decrypt secrets/.env.gpg)`

---

## Documentation

Browse offline documentation:
```
http://localhost/docs/
```

---

## Maintenance & Monitoring

- Logs: journalctl -u simulation.service
- System health: Netdata at http://localhost:19999

---

## Contribution

All changes should be GPG signed.
```
git commit -S -m "message"
```

---

## Contact

Author: Robert Shubert  
GitHub: [paracryptid](https://github.com/paracryptid)  
License: MIT

