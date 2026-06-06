# XNet-NGO APT Repository

This repository hosts Debian/Ubuntu packages for XNet-NGO tools.

## Available packages

- `aiope` (`amd64`)

## Quick install (Debian/Ubuntu)

### Recommended (signed repository)

If you host this repository with a published GPG key, configure it like this.
This is a template for signed deployments; provide and install your keyring file first.

```bash
echo "deb [signed-by=/usr/share/keyrings/xnet-ngo-archive-keyring.gpg] https://raw.githubusercontent.com/XNet-NGO/apt/main stable main" | sudo tee /etc/apt/sources.list.d/xnet-ngo.list
```

### Current repository state (unsigned)

WARNING: This repository currently does not publish a signed `InRelease`/`Release.gpg`.
Using `trusted=yes` disables APT signature verification and can expose systems to malicious packages.
Use this only in controlled environments you trust.

1. Add the repository:

```bash
echo "deb [trusted=yes] https://raw.githubusercontent.com/XNet-NGO/apt/main stable main" | sudo tee /etc/apt/sources.list.d/xnet-ngo.list
```

2. Update package indexes:

```bash
sudo apt update
```

3. Install package:

```bash
sudo apt install aiope
```

## Verify package metadata

You can inspect the repository metadata at:

- `dists/stable/Release`
- `dists/stable/main/binary-amd64/Packages`
