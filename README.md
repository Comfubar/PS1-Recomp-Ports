<div align="center">

# PS1 Recomp Ports

**Native Windows ports of PlayStation games, built on your PC from your own disc**

[![License: MIT](https://img.shields.io/github/license/Comfubar/PS1-Recomp-Ports)](LICENSE)
[![Platform](https://img.shields.io/badge/platform-Windows%20x64-0078D6)](#what-you-supply)
[![Recompiler](https://img.shields.io/badge/recompiler-RecompOne-555)](https://github.com/Comfubar/RecompOne-PS1Ports)

</div>

## Ports

| Game | Region / serial | Players | Status | Download | Repository |
|---|---|---|---|---|---|
| Know Your Role Recomp (2000 wrestling game) | NTSC-U · SLUS-01234 | 1-4 (automatic multitap) | released, v0.2.0 · [what works](https://github.com/Comfubar/KnowYourRoleRecomp/blob/main/docs/STATUS.md) | [![Download](https://img.shields.io/badge/Download-win--x64.zip-2ea44f)](https://github.com/Comfubar/KnowYourRoleRecomp/releases/latest/download/KnowYourRole-win-x64.zip) | [KnowYourRoleRecomp](https://github.com/Comfubar/KnowYourRoleRecomp) |

## How the ports work

Native PC ports of PlayStation games, made with the [RecompOne](https://github.com/BlackLabelHQ/RecompOne) static
recompiler. Each game's MIPS code is translated to C# ahead of time and runs on RecompOne's runtime, with no
emulator core.

**No game data is distributed here or in any port.** Every port ships one program that, on its first run, builds the
game on your PC from your own disc, and afterwards is the game's launcher (play, controllers, display, saves).

## What you supply

- Your own, legally obtained disc image of the exact release listed for the port (checked by SHA-256)
- Windows 10/11 x64 with an OpenGL 3.3 graphics driver
- No BIOS file: the runtime reimplements the BIOS calls

Controllers work through SDL (Xbox, PlayStation 4/5 without extra tools, Switch, 8BitDo and generic pads, USB and
Bluetooth), plus the keyboard. Each port's page lists which controllers were tested on real hardware.

## Runtime and recompiler

The ports use [RecompOne-PS1Ports](https://github.com/Comfubar/RecompOne-PS1Ports), a fork of RecompOne that keeps
the upstream history and adds what these ports needed: games made of several programs loaded at the same address,
split builds, reference bytes read from the player's disc, a DualShock with vibration, multitap and 4 players,
controller hot-plug and duplicate detection, and crash reports.

## License

The catalog is MIT licensed. Each port and RecompOne carry their own licenses. The games belong to their owners;
these are unofficial fan projects, not affiliated with or endorsed by the games' publishers, developers or Sony
Interactive Entertainment. Names are used only to identify compatibility.
