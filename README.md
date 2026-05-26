# Install NetVibe CLI on Windows

NetVibe CLI can be installed on Windows using the Scoop package manager.

## Prerequisites

If Scoop is not installed, open PowerShell and run:

```powershell
Set-ExecutionPolicy RemoteSigned -Scope CurrentUser
irm get.scoop.sh | iex
```

Verify the installation:

```powershell
scoop --version
```

## Add the NetVibe Bucket

Add the NetVibe Scoop bucket:

```powershell
scoop bucket add netvibe https://github.com/Manni-MinM/scoop-netvibe
```

## Install NetVibe CLI

Install the latest version:

```powershell
scoop install netvibe-cli
```

Verify the installation:

```powershell
netvibe-cli --help
```

## Configure NetVibe CLI

Run the setup command and enter your Vibepass when prompted:

```powershell
netvibe-cli setup
```

Configuration is stored locally and reused for future runs.

## Run NetVibe CLI

### Test Mode

Run NetVibe interactively and print logs to the terminal:

```powershell
netvibe-cli test
```

Test mode is useful for:

- verifying connectivity
- validating configuration
- debugging WebRTC sessions

### Daemon Mode

Run NetVibe continuously in the background:

```powershell
netvibe-cli daemon
```

Typical use cases include:

- long running measurement nodes
- persistent broadband monitoring
- server deployments

## Upgrade NetVibe CLI

Update Scoop and upgrade NetVibe CLI:

```powershell
scoop update
scoop update netvibe-cli
```

## Uninstall NetVibe CLI

Remove NetVibe CLI:

```powershell
scoop uninstall netvibe-cli
```

## Installation Location

Scoop installs NetVibe under:

```text
~/scoop/apps/netvibe-cli/current/
```

The executable is automatically added to your PATH.

## Troubleshooting

If Scoop commands fail due to PowerShell execution policy restrictions, run:

```powershell
Set-ExecutionPolicy RemoteSigned -Scope CurrentUser
```
