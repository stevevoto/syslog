## Quick Install (Fresh Server)

```bash
# 1. Extract the package
tar -xzf siem-syslog-1.4.7-*.tar.gz
cd siem-v10

# 2. Run the installer (requires sudo)
sudo bash install.sh
```

The installer will prompt for:
- **Admin username** — your first admin account
- **Admin password** — must be strong (8+ chars, mixed case)
- **Agent shared key** — used by the syslog agent scripts

It then:
- Creates a `siem-syslog` system user
- Installs Node.js 20 if not present
- Installs npm dependencies
- Sets up data directory at `/var/lib/siem-syslog/`
- Creates and starts the `siem-syslog` systemd service
- Generates a self-signed TLS certificate for encrypted syslog

---
