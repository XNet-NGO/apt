# XNet-NGO Package Repository

GPG-signed Debian/Ubuntu and RPM packages for XNet-NGO projects.

## Packages

| Package | Version | Architectures |
|---------|---------|---------------|
| `aiope` | 0.2.0 | amd64, arm64, armhf (deb) / x86_64, aarch64, armv7hl (rpm) |

## Install — Debian/Ubuntu (APT)

```bash
curl -fsSL https://raw.githubusercontent.com/XNet-NGO/apt/main/public-key.asc \
  | sudo gpg --dearmor -o /usr/share/keyrings/xnet-ngo-archive-keyring.gpg

echo "deb [signed-by=/usr/share/keyrings/xnet-ngo-archive-keyring.gpg] https://raw.githubusercontent.com/XNet-NGO/apt/main stable main" \
  | sudo tee /etc/apt/sources.list.d/xnet-ngo.list

sudo apt update && sudo apt install aiope
```

## Install — RHEL/Fedora/openSUSE (RPM)

```bash
sudo rpm --import https://raw.githubusercontent.com/XNet-NGO/apt/main/public-key.asc

sudo tee /etc/yum.repos.d/xnet-ngo.repo <<'EOF'
[xnet-ngo]
name=XNet-NGO
baseurl=https://raw.githubusercontent.com/XNet-NGO/apt/main/rpm-repo
enabled=1
gpgcheck=1
gpgkey=https://raw.githubusercontent.com/XNet-NGO/apt/main/public-key.asc
EOF

sudo dnf install aiope
```

## Signing Key

All packages and repository metadata are signed with GPG.

- **Key ID:** `77B6948E45E00E47`
- **Fingerprint:** `4460 9046 4838 1965 FD68 E711 77B6 948E 45E0 0E47`
- **UID:** `XNet-NGO <admin@xnet.ngo>`
- **Type:** RSA-4096
- **Public key:** [`public-key.asc`](public-key.asc)

## Repository Structure

```
├── dists/stable/
│   ├── InRelease          (clearsigned)
│   ├── Release.gpg        (detached signature)
│   └── main/binary-{amd64,arm64,armhf}/Packages
├── pool/main/             (.deb packages)
├── rpm-repo/              (signed .rpm + repodata)
└── public-key.asc
```
