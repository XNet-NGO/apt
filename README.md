# XNet-NGO APT & RPM Repository

Signed Debian/Ubuntu and RPM packages for XNet-NGO tools.

## Available packages

- `aiope` — amd64, arm64, armhf (deb) / x86_64, aarch64, armv7hl (rpm)

## Debian/Ubuntu (APT) — signed

```bash
curl -fsSL https://raw.githubusercontent.com/XNet-NGO/apt/main/public-key.asc | sudo gpg --dearmor -o /usr/share/keyrings/xnet-ngo-archive-keyring.gpg
echo "deb [signed-by=/usr/share/keyrings/xnet-ngo-archive-keyring.gpg] https://raw.githubusercontent.com/XNet-NGO/apt/main stable main" | sudo tee /etc/apt/sources.list.d/xnet-ngo.list
sudo apt update
sudo apt install aiope
```

## RHEL/Fedora/openSUSE (RPM) — signed

```bash
sudo rpm --import https://raw.githubusercontent.com/XNet-NGO/apt/main/public-key.asc
sudo tee /etc/yum.repos.d/xnet-ngo.repo <<REPO
[xnet-ngo]
name=XNet-NGO
baseurl=https://raw.githubusercontent.com/XNet-NGO/apt/main/rpm-repo
enabled=1
gpgcheck=1
gpgkey=https://raw.githubusercontent.com/XNet-NGO/apt/main/public-key.asc
REPO
sudo dnf install aiope
```
