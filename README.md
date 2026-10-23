# Zinetic Endpoint downloads

Release files for Zinetic Endpoint, the Zinetic agent for Windows, macOS and
Linux devices. The source code is not published here.

## Install

macOS 12 or later, or Linux (x86_64 or arm64) with systemd 250 or later, in a
terminal:

```bash
curl -fsSL https://cli.zinetic.net/endpoint/install.sh | bash
```

Windows 10 or 11, in PowerShell:

```powershell
irm https://cli.zinetic.net/endpoint/install.ps1 | iex
```

On Windows the installer asks for administrator rights itself. Do not run the
`curl … | bash` line in PowerShell, where `curl` is a different command and
`bash` does not exist. In Git Bash, MSYS2 or WSL it works: it starts the
PowerShell installer for you. Then run setup in a new PowerShell window.

Then set up the device:

```bash
zinetic endpoint setup
```

Installing gives no access to anything by itself. Setup enrolls the device only
after you sign in to your organization and approve the device.

## Check a download by hand

Each release lists the SHA-256 of its files in `SHA256SUMS`:

```bash
shasum -a 256 -c SHA256SUMS --ignore-missing
```

Test releases, named `p1-04-uat-…`, are not signed or notarized. Use them only
for authorized testing.
