# Shiny Hunting PokeBot
 
**Shiny Hunting Pokebot** is a shiny hunting bot, written in Python that runs 'libmgba' + mGBA Python bindings under the hood. Currently all of the Generation 3 GBA Pokemon games are support.

Initially created to complete a Shiny Living Dex. The plans for this bot are to support all supported Languages for the generation 3 Pokemon games. As well as be able to hunt for competitive, specific stat Pokemon.

The intent of this bot is not to cheat for shinies but to transfer the generation 3 Pokemon games into a somewhat idel game, to help ease the pain that is hunting in these specific set of games. 

The bot is frame perfect and can technically cheat by reading data form any point in memory and manipulate RNG. By default, it will attempt to perform actions as if a human were playing to make the gameplay as representative as possible. For ex:
- Starter Pokemon are generated just 1 frame aftger confirming the starter selection, the bot will wait until the battle begins, and the starter Pokemon sprite is visible before soft resetting.
- It is possible to peek inside un-hatched Pokemon eggs to view stats and their shininess as soon as they are received from the Daycare man. The bot instead waits until the eggs are fully hatched before checking and logging them.
  
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
