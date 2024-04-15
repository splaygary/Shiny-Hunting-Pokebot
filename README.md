# Shiny Hunting PokeBot
 
**Shiny Hunting Pokebot** is a shiny hunting bot, written in Python that runs 'libmgba' + mGBA Python bindings under the hood. Currently all of the Generation 3 GBA Pokemon games are support.

Initially created to complete a Shiny Living Dex. The intent of this bot is not to cheat for shinies but to transfer the generation 3 Pokemon games into a somewhat idel game, to help ease the pain that is hunting in these specific set of games. 

The bot is frame perfect and can technically cheat by reading data form any point in memory and manipulate RNG. By default, it will attempt to perform actions as if a human were playing to make the gameplay as representative as possible. For example:
- Starter Pokemon are generated just 1 frame after confirming the starter selection, the bot will wait until the battle begins, and the starter Pokemon sprite is visible before soft resetting.
- It is possible to peek inside un-hatched Pokemon eggs to view stats and their shininess as soon as they are received from the Daycare man. The bot instead waits until the eggs are fully hatched before checking and logging them.

# Getting Started

## Supported Operating Systems

- Windows
- MacOS
- Linux, tested and confirmed working on the following distros:
  - Ubuntu 23.04, 23.10
  
## Requirements
### Windows
- [Python 3.12](https://www.python.org/downloads/windows/) **Windows installer 64-bit**
  - Tick `Add Python to PATH` when installing Python

### MacOS
- [Python 3.12](https://www.python.org/downloads/macos/) **macOS 64-bit universal2 installer** or `brew install python@3.12`
- mGBA 0.10.x `brew install mgba`

Note: `brew` requires [Homebrew](https://brew.sh/) to be installed.

### Linux
- [Python 3.12](https://www.python.org/downloads/source/) or `sudo apt install python3.12`
- Install the following packages with `apt` or appropriate package manager: `sudo apt install python3-distutils python3-tk libmgba0.10 portaudio19-dev`
- If `libmgba0.10` is not available on your distro, you can manually install the [mGBA 0.10.x .deb package](https://mgba.io/downloads.html) which includes `libmgba0.10`

## Download the Bot
To download the latest dev releases, go to the top of the repo page > click the green **Code** button > **Download ZIP**.

## Run the Bot
- Place some **official** Pokémon .gba ROMs into the `./roms/` folder
- Double click `pokebot.py` or run `python pokebot.py` in a terminal and follow the on-screen steps to create and/or select a profile

You **must** ensure you are able to escape battle **100% of the time**, otherwise the bot will get stuck.
If you have a save from mGBA that you'd like to import and use with the bot, then you will need to import the save state.

This bot is still in development, as such, functionality is subject to change - always make sure you back up your `./profiles/` folder before updating your bot! 

## Import a Save
- In mGBA (standalone), run a game and load into the save file
- **File** > **Save State File...** > **Save**
- Double click `pokebot.py` or run `python pokebot.py` in a terminal > type a profile **name** > click **Load Existing Save**
- Open the save state file you just saved
- A new bot profile will be created in the `./profiles/` folder, and launched
  
# Credits

Core functionality:

- [mGBA](https://github.com/mgba-emu/mgba)
- [libmgba-py](https://github.com/hanzi/libmgba-py/)

Inspiration for the project:

- [PokéBot NDS](https://github.com/wyanido/pokebot-nds/)

Big shoutout to the following projects for the decompiled symbol tables and other various data that played a big role
contributing to this project:

- [Pokémon Emerald decompilation](https://github.com/pret/pokeemerald) ([symbols](https://github.com/pret/pokeemerald/tree/symbols))
- [Pokémon Ruby and Sapphire decompilation](https://github.com/pret/pokeruby) ([symbols](https://github.com/pret/pokeruby/tree/symbols))
- [Pokémon FireRed and LeafGreen decompilation](https://github.com/pret/pokefirered) ([symbols](https://github.com/pret/pokefirered/tree/symbols))
