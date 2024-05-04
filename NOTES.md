# General modding notes

These are the collection of notes I've gathered while trying to mod Quake 2.

## Utility functions
- `gi.centerprintf(edict_t *ent, const char *fmt)`
    - prints text in-game in front of player, center of screen
- `gi.cprintf(edict_t *ent, int printlevel, const char *fmt)`
    - prints message to a player's console
- `gi.dprintf(const char *fmt)`
    - debug printf, prints to command line

## Movement
- There are two critical physics files:
    - g_phys.c      -> general physics engine
    - pmove.c       -> player movement
- struct pmove_t
    - defined in common/shared.h
- usercmd_t
    - defined in common/shared.h
    - contains a whole bunch of user movement commands, such as upmove, sidemove, etc.
    - maybe move double jump / dash / other player movement there?

## Combat
- T_Damage() function handles damage of all entities (defined in g_combat.c)

## edict_t (entities)
- Type of edict_s
    - edict_s defined in game.h

## Timers
- Look in g_main.c
    - EndDMLevel() & CheckDMRules()
- sv_init.c

## Checkpoints
- `src/game/g_trigger.c`
