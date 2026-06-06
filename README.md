# XNet-NGO APT & RPM Repository

Debian/Ubuntu and RPM packages for XNet-NGO tools.

## Available packages

- `aiope` — amd64, arm64, armhf (deb) / x86_64, aarch64, armv7hl (rpm)

## Debian/Ubuntu (APT)

```bash
echo "deb [trusted=yes] https://raw.githubusercontent.com/XNet-NGO/apt/main stable main" | sudo tee /etc/apt/sources.list.d/xnet-ngo.list
sudo apt update
sudo apt install aiope
```

## RHEL/Fedora/openSUSE (RPM)

```bash
sudo tee /etc/yum.repos.d/xnet-ngo.repo <<REPO
[xnet-ngo]
name=XNet-NGO
baseurl=https://raw.githubusercontent.com/XNet-NGO/apt/main/rpm-repo
enabled=1
gpgcheck=0
REPO
sudo dnf install aiope
```
