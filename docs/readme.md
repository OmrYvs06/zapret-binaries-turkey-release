# Why this project?
I just installed `zapret-v72.2` version ([link](https://github.com/bol-van/zapret/releases/tag/v72.2)) and configured it, after that I just pushed it here, thats all.

# How to use?

### Clone this project
```bash
git clone https://github.com/OmrYvs06/zapret-Turkey-V72.2-Release
```

### create /opt/zapret folder
```bash
sudo mkdir -p /opt/zapret
```
### copy our cloned folder contents to that folder
```bash
sudo cp -r ./zapret-Turkey-V72.2-Release/* /opt/zapret
```

### execute install_easy.sh in /opt/zapret folder
```bash
sudo bash /opt/zapret/install_easy.sh
```

after that, you only need to click enter until script ends.
next next next to all options (they all configured for turkey) and we are done.

if you want to remove unnecessery files after installation:
```bash
rm -rf ./zapret-Turkey-V72.2-Release
```

## Copy-paste installation
here is the one line command that do all in one removes unnecessery files (you will be prompted only for `sudo` password)
```bash
cd && git clone https://github.com/OmrYvs06/zapret-Turkey-V72.2-Release && sudo mkdir -p /opt/zapret && sudo cp -rf ./zapret-Turkey-V72.2-Release/* /opt/zapret && rm -rf ./zapret-Turkey-V72.2-Release && sudo bash /opt/zapret/install_easy.sh
```
or
```bash
cd && \
git clone https://github.com/OmrYvs06/zapret-Turkey-V72.2-Release && \
sudo mkdir -p /opt/zapret && \
sudo cp -rf ./zapret-Turkey-V72.2-Release/* /opt/zapret && \
rm -rf ./zapret-Turkey-V72.2-Release && \
sudo bash /opt/zapret/install_easy.sh
```


# Extras
These configurations no needed for zapret usage, but they improve the experience and privacy for system wide.
## 1. installing and setting up `dnscrypt-proxy`
if you want to install `dnscrypt-proxy` with `zapret`, you can follow [this](https://btt.community/t/linux-zapret-kurulum-rehberi/15989) guide (they cover only `NetworkManager` setup).

here is the guide using `dnscrypt-proxy` for the system uses `systemd-resolved`:
### installing dnscrypt-proxy

**Arch Linux**: `sudo pacman -S dnscrypt-proxy` </br>
**Fedora**: `sudo dnf install dnscrypt-proxy` </br>
**OpenSUSE**: `sudo zypper in dnscrypt-proxy` </br>
**Alpine Linux**: `sudo apk add dnscrypt-proxy` </br>
**Void Linux**: `sudo xbps-install -S dnscrypt-proxy` </br>
**Gentoo**: `emerge dnscrypt-proxy`

### edit dnscrypt-proxy config file
```bash
sudo nano /etc/dnscrypt-proxy/dnscrypt-proxy.toml
```
edit or add this lines
```bash
listen_addresses = ['127.0.0.1:53', '[::1]:53']
```
### enabling dnscrypt-proxy
```bash
sudo systemctl enable dnscrypt-proxy.service
sudo systemctl start dnscrypt-proxy.service
```

### setting up systemd resolved.conf file: open resolved.conf file
```bash
sudo nano /etc/systemd/resolved.conf
```
edit or add this lines
```bash
[Resolve]
DNS=127.0.0.1 ::1
EDNS0=yes
Domains=~.
```
### restart systemd-resolved
```bash
sudo systemctl restart systemd-resolved
```


