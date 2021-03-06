[comment]: # (GitHub README.md)

# GTA V Speedometer

[![Build status](https://ci.appveyor.com/api/projects/status/97b6m5xup9onnben?svg=true)](https://ci.appveyor.com/project/E66666666/gtavspeedo)

*Yet another* speedometer! NFSU-style, with support for NOS and Turbo.

![Preview](./preview.jpg)

## Requirements

* Grand Theft Auto V
* [ScriptHookV by Alexander Blade](http://www.dev-c.com/gtav/scripthookv/)

## Downloads

* [GTA5-Mods.com](https://www.gta5-mods.com/scripts/need-for-speed-underground-speedometer)

## Building

### Requirements

* [ScriptHookV SDK by Alexander Blade](http://www.dev-c.com/gtav/scripthookv/)
* [GTAVMenuBase](https://github.com/E66666666/GTAVMenuBase)
* [GTAVManualTransmission](https://github.com/E66666666/GTAVManualTransmission)

Mentioned requirements are partly submodules, so just init/update your cloned
repo and you should be good to go.

## Decorators

This script reads the following decorators:

* `int` - `ikt_speedo_nos`: Presence of a nitrous mod
* `float` - `ikt_speedo_nos_level`: Nitrous level, between 0.0f and 1.0f
* `int` - `nfsnitro_stage`: Nitrous kit upgrade level
* `float` - `nfsdrag_heat`: Drag HUD heat
* `bool` - `nfsdrag_showhud`: Drag HUD toggle

To make the green N2O bars appear in the speedometer, your mod has to set `ikt_speedo_nos` to 1 on the currently used vehicle, set it to 0 to remove.

N2O level ranges from 1.0f to 0.0f. Again, set `ikt_speedo_nos_level` to this level on the currently used vehicle.

N2O bars also appear for vehicles with a rocket boost - the rocket boost takes precedence over any external mods.
