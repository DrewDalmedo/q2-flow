# Yamagi Quake II - Flow Mod

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

## About Flow
Flow is an extended movement mod which aims to create a multiplayer FPS-Racing 
hybrid.

The mod adds 5 new movement abilities:

1. Double Jumping
    - To double jump, jump again once you're in the air.
2. Sliding
    - To slide, hold crouch while moving in the direction you want to slide in.
3. Super Jumping
    - To super jump, first crouch, then quickly hit the jump key to jump higher than normal.
4. Dashing
    - To dash, use the dash key (default SHIFT).
5. Stomping
    - To stomp, crouch while in the air. This will send you immediately falling back down to the ground.

Additionally, all damage has been disabled. In place of traditional damage, players
can now inflict debuffs on opponents which disable their advanced movement abilites,
depending on which weapon they use. Additionally, damage from all weapons now temporarily 
slows the player.

The weapons that affect movement are:

1. Blaster - Disables Dash
2. Hyperblaster - Disables Slide
3. Shotgun - Disables Double Jump
4. Machinegun - Disables Stomp
5. Railgun - Disables Super Jump

At the end of each game, the total time the game took is saved locally. On Linux,
this location is `~/.yq2/flow/time.txt`, where `flow` is the name of the mod folder.

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

### Compiling and running from source

For compiling and running the game in the same step, make sure you have a directory
named `modfiles` at the root of the project. Put all your `.pak` files from your vanilla
Quake 2 installation in there, and then type: 

```bash
make run
``` 

in the root of the project.

### Generating a mod folder
There is a separate `make` target provided for generating this folder. After copying all
your `.pak` files to the `modfiles` folder in the root of the project directory, run the following command:

```bash
make modfolder
```

Then, after the build target finishes, run the game by typing:

```bash
bash ./launch.sh
```
