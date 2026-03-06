# Install NetVibe CLI on Windows (via Scoop)

NetVibe CLI can be installed on Windows using the **Scoop package manager**.

---

# 1. Install Scoop (if not already installed)

Open **PowerShell** and run:

```powershell
Set-ExecutionPolicy RemoteSigned -Scope CurrentUser
irm get.scoop.sh | iex
```

Verify installation:

```powershell
scoop --version
```

---

# 2. Add the NetVibe Scoop Bucket

```powershell
scoop bucket add netvibe https://github.com/Manni-MinM/scoop-netvibe
```

---

# 3. Install NetVibe CLI

```powershell
scoop install netvibe-cli
```

---

# 4. Verify Installation

```powershell
netvibe-cli --help
```

---

# NetVibe CLI Usage

## 1. Initial Setup (Add Vibepass)

Run the setup command and enter your **Vibepass** when prompted.

```powershell
netvibe-cli setup
```

This will store your configuration in:

```
~/.netvibe-cli/config.json
```

---

## 2. Run Test Mode

Test mode runs the NetVibe answerer interactively and prints logs to the terminal.

```powershell
netvibe-cli test
```

This is useful for:

- debugging connectivity
- verifying WebRTC connection
- validating configuration

---

## 3. Run Daemon Mode

Daemon mode runs the NetVibe answerer continuously in the background.

```powershell
netvibe-cli daemon
```

Typical usage:

- long running NetVibe measurement nodes
- deployment on servers
- persistent monitoring

---

# Updating NetVibe CLI

```powershell
scoop update
scoop update netvibe-cli
```

---

# Uninstalling NetVibe CLI

```powershell
scoop uninstall netvibe-cli
```

---

# Notes

Scoop installs NetVibe to:

```
~/scoop/apps/netvibe-cli/current/
```

The binary is automatically added to your **PATH**.

---

# Troubleshooting

If Scoop commands fail, ensure PowerShell execution policy allows scripts:

```powershell
Set-ExecutionPolicy RemoteSigned -Scope CurrentUser
```
