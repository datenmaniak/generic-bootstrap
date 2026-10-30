# Fedora, AlmaLinux and RHEL Migration Steps

## Install GUI apps (essential)

```bash
flatpak remote-add --if-not-exists flathub https://dl.flathub.org/repo/flathub.flatpakrepo
```

```bash
flatpak install -y md.obsidian.Obsidian com.obsproject.Studio \
org.videolan.VLC com.vivaldi.Vivaldi
```

## Start CLI Bootstrapping

```bash
git clone https://github.com/datenmaniak/generic-bootstrap.git
```

## Install packages according your releases: Atomic o rpm/dnf

```bash
cd ~/generic-bootstrap
./fedora-edition

# For Atomic
./fedora-atomic
```

- Reboot the Atomic Workstation or

- Re-Open the terminal

## Change default Shell

```bash
sudo usermod --shell /usr/bin/zsh $USER
```

- Reboot Again or Re-open console

- Ignore zsh configuration

```bash
# Exit zsh configuration
q

```

## Permission

- Copy the private key

```bash
cd ~/generic-bootstrap
cp private-keys  ~/generic-bootstrap/privkey.asc
```

## CLI Setting setup: Install Mise and dotfiles

```bash
./setup
```
