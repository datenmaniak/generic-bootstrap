# Fedora (Sway Atomic, Silverblue or Bazzite) Migration Steps

## Install GUI apps (essential)

```bash
flatpak remote-add --if-not-exists flathub https://dl.flathub.org/repo/flathub.flatpakrepo
```

```bash
flatpak install -y md.obsidian.Obsidian com.obsproject.Studio \
org.videolan.VLC com.vivaldi.Vivaldi
```

```plaintext
Resolution 1920x1080
25 PAL
```

## Bootstrapping the workstation

- Mount USB Key

```bash
sudo mount /dev/sdX /mnt

mkdir ~/workstation_bootstrap
cp /mnt/* ~/workstation_bootstrap
sudo umount /mnt/
```

- Unplug USB Key

## Install packages

```bash
cd ~/workstation_bootstrap
./fedora
```

- Reboot the Workstation

- Open the terminal `Alacritty`

## Change default Shell

```bash
sudo usermod --shell /usr/bin/zsh $USER
```

- Reboot Again

## Setting up SSH Keys, Install Mise and dotfiles

```bash
./setup
```
