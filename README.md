# XNet-NGO APT Repository

This repository hosts Debian/Ubuntu packages for XNet-NGO tools.

## Available package(s)

- `aiope` (`amd64`)

## Quick install (Debian/Ubuntu)

### Recommended (signed repository)

If you host this repository with a GPG key, configure it like this:

```bash
echo "deb [signed-by=/usr/share/keyrings/xnet-ngo-archive-keyring.gpg] https://raw.githubusercontent.com/XNet-NGO/apt/main stable main" | sudo tee /etc/apt/sources.list.d/xnet-ngo.list
```

### Current repository state (unsigned)

This repository currently does not publish a signed `InRelease`/`Release.gpg`, so APT needs explicit trust override.
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
