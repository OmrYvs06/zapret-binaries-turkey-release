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




