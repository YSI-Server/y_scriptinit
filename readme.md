# y_scriptinit

Provides several new initialisation callbacks to avoid knowing what the current script type is.  The full initialisation order is:

* `OnCodeInit` - Called first to generate code.  No advanced YSI features are available here (including hooking this callback).
* `OnJITCompile` - If this is running in the JIT.
* `PREINIT__` - Special init functions, used for tiny setup code (more light-weight than hooks).
* `OnScriptInit` - Called when this script starts.  This is the most important callback as it is called once first, regardless of the script type, and all YSI features are now available.
* `POSTINIT__` - Special init functions, used for tiny setup code (more light-weight than hooks).
* `OnFilterScriptInit` - If this is a filterscript.
* `OnGameModeInit` - Once in a gamemode, possibly multiple times in a filterscript.

The shutdown order is:

* `OnGameModeExit` - Once in a gamemode, possibly multiple times in a filterscript.
* `OnFilterScriptExit` - If this is a filterscript.
* `OnScriptExit` - Called when this script ends, regardless of the type.


[![sampctl](https://shields.southcla.ws/badge/sampctl-y_scriptinit-2f2f2f.svg?style=for-the-badge)](https://github.com/YSI-Server/y_scriptinit)

## Installation

To install just this one library:

```bash
sampctl package install YSI-Server/y_scriptinit
```

Include in your code and begin using the library:

```pawn
#include <YSI-Server/y_scriptinit>
```

## Documentation

* [Quick Start](YSI-Server/y_scriptinit/quick-start.md) - One very simple example of getting started with this library.
* [Features](YSI-Server/y_scriptinit/features.md) - More features and examples.
* [FAQs](YSI-Server/y_scriptinit/faqs.md) - Frequently Asked Questions, including errors and solutions.
* [API](YSI-Server/y_scriptinit/api.md) - Full list of all functions and their meaning.
* [Internal](YSI-Server/y_scriptinit/internal.md) - Internal developer documentation for the system.

## Testing

To test, simply run the package:

```bash
sampctl package run
```

# YSI

## General Information

* [installation](installation.md)
* [troubleshooting](troubleshooting.md)
* [YSI_COMPATIBILTY_MODE](YSI_COMPATIBILTY_MODE.md)
* [What does YSI stand for?](acronym.md)

## Libraries

### Coding

PAWN scripting improvements (i.e. new language features).

* [y_functional](https://github.com/YSI-Coding/y_functional)
* [y_hooks](https://github.com/YSI-Coding/y_hooks)
* [y_inline](https://github.com/YSI-Coding/y_inline)
* [y_malloc](https://github.com/YSI-Coding/y_malloc)
* [y_remote](https://github.com/YSI-Coding/y_remote)
* [y_stringhash](https://github.com/YSI-Coding/y_stringhash)
* [y_timers](https://github.com/YSI-Coding/y_timers)
* [y_unique](https://github.com/YSI-Coding/y_unique)
* [y_va](https://github.com/YSI-Coding/y_va)

### Core

Core libraries, used almost everywhere else.

* [y_als](https://github.com/YSI-Core/y_als)
* [y_cell](https://github.com/YSI-Core/y_cell)
* [y_debug](https://github.com/YSI-Core/y_debug)
* [y_master](https://github.com/YSI-Core/y_master)
* [y_profiling](https://github.com/YSI-Core/y_profiling)
* [y_testing](https://github.com/YSI-Core/y_testing)
* [y_utils](https://github.com/YSI-Core/y_utils)

### Data

Data structures and algorithms.

* [y_bintree](https://github.com/YSI-Data/y_bintree)
* [y_bit](https://github.com/YSI-Data/y_bit)
* [y_iterate](https://github.com/YSI-Data/y_iterate)
* [y_hashmap](https://github.com/YSI-Data/y_hashmap)
* [y_jaggedarray](https://github.com/YSI-Data/y_jaggedarray)
* [y_playerarray](https://github.com/YSI-Data/y_playerarray)
* [y_playerset](https://github.com/YSI-Data/y_playerset)
* [y_sortedarray](https://github.com/YSI-Data/y_sortedarray)
* [y_sparsearray](https://github.com/YSI-Data/y_sparsearray)

### Extra

Optional features.

* [y_extra](https://github.com/YSI-Extra/y_extra)
* [y_files](https://github.com/YSI-Extra/y_files)
* [y_streamer_plugin](https://github.com/YSI-Extra/y_streamer_plugin)

### Game

Libraries that provide information about the game.

* [y_vehicledata](https://github.com/YSI-Game/y_vehicledata)

### Players

Libraries for managing players.

* [y_groups](https://github.com/YSI-Players/y_groups)
* [y_languages](https://github.com/YSI-Players/y_languages)
* [y_text](https://github.com/YSI-Players/y_text)
* [y_users](https://github.com/YSI-Players/y_users)

### Server

Libraries for controlling the server.

* [y_colours](https://github.com/YSI-Server/y_colours)
* [y_flooding](https://github.com/YSI-Server/y_flooding)
* [y_lock](https://github.com/YSI-Server/y_lock)
* [y_punycode](https://github.com/YSI-Server/y_punycode)
* [y_scriptinit](https://github.com/YSI-Server/y_scriptinit)
* [y_stringise](https://github.com/YSI-Server/y_stringise)
* [y_td](https://github.com/YSI-Server/y_td)

### Storage

Libraries for interacting with persistent data.

* [y_amx](https://github.com/YSI-Storage/y_amx)
* [y_bitmap](https://github.com/YSI-Storage/y_bitmap)
* [y_ini](https://github.com/YSI-Storage/y_ini)
* [y_php](https://github.com/YSI-Storage/y_php)
* [y_svar](https://github.com/YSI-Storage/y_svar)
* [y_uvar](https://github.com/YSI-Storage/y_uvar)
* [y_xml](https://github.com/YSI-Storage/y_xml)

### Visual

Libraries that have in-game visible effects.

* [y_areas](https://github.com/YSI-Visual/y_areas)
* [y_classes](https://github.com/YSI-Visual/y_classes)
* [y_commands](https://github.com/YSI-Visual/y_commands)
* [y_dialog](https://github.com/YSI-Visual/y_dialog)
* [y_loader](https://github.com/YSI-Visual/y_loader)
* [y_properties](https://github.com/YSI-Visual/y_properties)
* [y_races](https://github.com/YSI-Visual/y_races)
* [y_zonenames](https://github.com/YSI-Visual/y_zonenames)
* [y_zonepulse](https://github.com/YSI-Visual/y_zonepulse)
