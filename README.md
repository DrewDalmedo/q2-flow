# Yamagi Quake II

Yamagi Quake II is an enhanced client for id Software's Quake
II with focus on offline and coop gameplay. Both the gameplay and the graphics
are unchanged, but many bugs in the last official release were fixed and some
nice to have features like widescreen support and a modern OpenGL 3.2 renderer
were added. Unlike most other Quake II source ports Yamagi Quake II is fully 64-bit
clean. It works perfectly on modern processors and operating systems. Yamagi
Quake II runs on nearly all common platforms; including FreeBSD, Linux, NetBSD,
OpenBSD, Windows and macOS (experimental).

This code is built upon Icculus Quake II, which itself is based on Quake II
3.21. Yamagi Quake II is released under the terms of the GPL version 2. See the
LICENSE file for further information.

## Documentation

Before asking any question, read through the documentation! The current
version can be found here: [doc/010_index.md](doc/010_index.md)

## Releases

The official releases (including Windows binaries) can be found at our
homepage: https://www.yamagi.org/quake2  
**Unsupported** preview builds for Windows can be found at
https://deponie.yamagi.org/quake2/misc/

## Build Instructions
On Linux, build dependencies will vary from distro to distro.

Ubuntu 22.04 dependencies:
- build-essential
- libcurl4-gnutls-dev
- libsdl2-dev
- libopenal-dev

To install these dependencies on Ubuntu 22.04, run the following command:

```sh
sudo apt install -y build-essential libcurl4-gnutls-dev libsdl2-dev libopenal-dev 
```

Then, at the root of the project folder, run `make`.
