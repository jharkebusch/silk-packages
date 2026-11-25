# Silk packages

Signed pacman packages of Silk, a desktop built on Arch Linux and Hyprland.
GitHub Pages serves them from the `gh-pages` branch, which CI replaces with
every release.

Silk's installer sets this repo up. By hand:

```
sudo pacman-key --add silk.asc
sudo pacman-key --lsign-key 357F090618E526D6FB40BDA829875BAD131AECC8
```

and in `/etc/pacman.conf`:

```
[silk]
Server = https://jharkebusch.github.io/silk-packages/$arch
```

Then `sudo pacman -Syu silk-meta`.

Silk is licensed under the PolyForm Noncommercial License 1.0.0 (see
`LICENSE.md`): you may use, change and share it for any noncommercial
purpose. The `silk-hyprbars` package is the hyprbars plugin from
hyprland-plugins, under its own BSD 3-Clause licence.
