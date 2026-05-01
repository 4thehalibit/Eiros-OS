# Eiros — NixOS on Framework Laptop 16

Personal NixOS setup built on the [Eiros](https://github.com/lcleveland/eiros) framework.

## Repos

| Repo | Purpose |
|------|---------|
| [eiros.users.vwestberg](https://github.com/4thehalibit/eiros.users.vwestberg) | User configuration — apps, keybinds, monitor layout, shell aliases |
| [eiros.hardware.vwestberg](https://github.com/4thehalibit/eiros.hardware.vwestberg) | Hardware configuration for Framework Laptop 16 |
| [ninjaone-nixos](https://github.com/4thehalibit/ninjaone-nixos) | NixOS module for the NinjaOne RMM remote access client |

## How they fit together

`eiros.users.vwestberg` is the main config flake. It pulls in `ninjaone-nixos` as a flake input and is loaded alongside `eiros.hardware.vwestberg` at rebuild time via the `rebuild` alias.
