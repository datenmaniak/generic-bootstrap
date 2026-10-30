# Fedora, AlmaLinux and RHEL Migration Steps

## Install GUI apps (essential)

```bash
flatpak remote-add --if-not-exists flathub https://dl.flathub.org/repo/flathub.flatpakrepo
```

```bash
flatpak install -y md.obsidian.Obsidian com.obsproject.Studio \
org.videolan.VLC com.vivaldi.Vivaldi
```

```bash
git clone https://github.com/datenmaniak/generic-bootstrap.git
```

## Install packages

```bash
cd ~/generic_bootstrap
./fedora-edition
```

- Reboot the Workstation/Server (For Atomic Releases) or Reboot the terminal

- Open the terminal

## Change default Shell

```bash
sudo usermod --shell /usr/bin/zsh $USER
```

- Reboot Again / Restart console

## Setting up SSH Keys, Install Mise and dotfiles

- Copy the private key

```bash
cp private-keys  ~/generic_bootstrap/
```

## CLI Setting setup

```bash
./setup
```
