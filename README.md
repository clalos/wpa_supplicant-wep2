# wpa_supplicant-wep2

[![AUR version](https://img.shields.io/aur/version/wpa_supplicant-wep2?logo=archlinux&color=1793d1)](https://aur.archlinux.org/packages/wpa_supplicant-wep2)
[![AUR votes](https://img.shields.io/aur/votes/wpa_supplicant-wep2)](https://aur.archlinux.org/packages/wpa_supplicant-wep2)

> wpa_supplicant with WEP support enabled, tracking the official Arch package.

This repository is the source for the [`wpa_supplicant-wep2`](https://aur.archlinux.org/packages/wpa_supplicant-wep2) AUR package.

## Differences from the official package

The only change is enabling `CONFIG_WEP=y` in the build configuration. Everything else (version, patches, dependencies) tracks the official [`wpa_supplicant`](https://archlinux.org/packages/core/x86_64/wpa_supplicant/) package exactly.

This is useful for connecting to legacy networks that still use WEP encryption via NetworkManager.

## Installation

**Using an AUR helper:**

```bash
paru -S wpa_supplicant-wep2
# or
yay -S wpa_supplicant-wep2
```

**Manually:**

```bash
git clone https://aur.archlinux.org/wpa_supplicant-wep2.git
cd wpa_supplicant-wep2
makepkg -si
```

After installing, restart the relevant services:

```bash
sudo systemctl restart wpa_supplicant NetworkManager
```

## Updates

A [GitHub Actions workflow](.github/workflows/update-aur.yml) checks weekly for new upstream releases and automatically syncs the PKGBUILD and pushes to AUR.

## Contributing

Open issues and PRs on [GitHub](https://github.com/clalos/wpa_supplicant-wep2). For package-specific discussion, see the [AUR comments](https://aur.archlinux.org/packages/wpa_supplicant-wep2).

## License

The PKGBUILD and build configuration are based on the official Arch Linux package. The packaged software is licensed under [BSD-3-Clause](https://w1.fi/cgit/hostap/plain/COPYING).
