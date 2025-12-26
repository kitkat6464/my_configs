<div align="center">
ADDING THIS CAUSE INCASE I HIT MY HEAD, AND FORGET HOW TO DO STUFF
</div>

> [!TIP]
> Install Using Cachy Minimal or Arch Minimal (No Desktop Option)

## Step 1: Install Dank Shell Using That Beautiful TTY:

[Dank Shell Installation Guide](https://danklinux.com/docs/getting-started)

## Step 2: Install Dank Greeter Cause That's Hot AF:

[Dank Greeter Installation Guide](https://danklinux.com/docs/dankgreeter/installation)

## Step 3: Install Missing Stuff:
(This Adds Missing Stuff Like File Manager, Photo Viewer, Video Player, Music Player, Missing Deps For Consistency, and Gamescope Tiling Support)

```shell
curl -fsSL https://raw.githubusercontent.com/kitkat6464/my_configs/refs/heads/cachyos/AfterInstall | sh
```

## Step 4: Install's Lact and QT Theming Support From The AUR:

```shell
curl -fsSL https://raw.githubusercontent.com/kitkat6464/my_configs/refs/heads/cachyos/AfterInstallAur | sh
```

## Step 5: Setup File Extension Support:

```shell
cd .config
```

```shell
wget https://raw.githubusercontent.com/kitkat6464/my_configs/refs/heads/cachyos/.config/mimeapps.list
```

## Step 6: Setup Secondary Drive Access:

Make Mounting Folder For Secondary Drive.

```shell
sudo mkdir /mnt/games
```

> [!TIP]
> Using This Command In The Terminal Will Find Your Drive UUID -> lsblk -f

Add Drive To fstab File:

```shell
sudo nano /etc/fstab
```

> UUID=YOURDRIVEUUID /mnt/games     btrfs   defaults,noatime,compress=zstd,commit=120 0 0

Mount Your New Drive:

```shell
sudo systemctl daemon-reload
```

```shell
sudo mount -a
```
