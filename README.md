# Zinetic Endpoint downloads

Release files for Zinetic Endpoint, the Zinetic agent for macOS and Windows
devices. The source code is not published here.

## Install

macOS 12 or later, in Terminal:

```bash
curl -fsSL https://cli.zinetic.net/endpoint/install.sh | bash
```

Windows 10 or 11, in PowerShell opened with **Run as administrator**:

```powershell
irm https://cli.zinetic.net/endpoint/install.ps1 | iex
```

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
