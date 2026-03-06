````markdown
# Install NetVibe CLI on Windows (via Scoop)

NetVibe CLI can be installed easily on Windows using the **Scoop package manager**.

## 1. Install Scoop (if not already installed)

Open **PowerShell** and run:

```powershell
Set-ExecutionPolicy RemoteSigned -Scope CurrentUser
irm get.scoop.sh | iex
````

Verify installation:

```powershell
scoop --version
```

---

## 2. Add the NetVibe Scoop Bucket

```powershell
scoop bucket add netvibe https://github.com/Manni-MinM/scoop-netvibe
```

---

## 3. Install NetVibe CLI

```powershell
scoop install netvibe-cli
```

---

## 4. Verify Installation

```powershell
netvibe-cli --help
```

---

## 5. Update NetVibe CLI

```powershell
scoop update
scoop update netvibe-cli
```

---

## 6. Uninstall (Optional)

```powershell
scoop uninstall netvibe-cli
```

---

# Notes

* Scoop installs NetVibe into:

```
~/scoop/apps/netvibe-cli/current/
```

* The executable will automatically be added to your **PATH**.

---

# Troubleshooting

If Scoop commands fail, ensure PowerShell execution policy allows scripts:

```powershell
Set-ExecutionPolicy RemoteSigned -Scope CurrentUser
```

```
```
