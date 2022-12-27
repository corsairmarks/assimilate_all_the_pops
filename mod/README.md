# Overview

Summary

# Changes

Allows regular empires to select Synthetic Evolution, The Flesh is Weak, Mind Over Matter, and/or Engineered Evolution.  Allows Driven Assimilator machine empires to select both Organo-Machine Interfacing and Synthetic Age. Allows hive-minded empires to select both Organo-Machine Interfacing and Engineered Evolution.

## Compatibility

This mod overrides the seven ascension path-related ascension perks. It is not compatible with other mods that alter Synthetic Evolution, Synthetic Age, The Flesh is Weak, Organo-Machine Interfacing (both versions), Mind Over Matter, and Engineered Evolution.

Built for Stellaris version 3.6 "Orion."  Not compatible with achievements.

### Not Included in "Subtle Polish"

This mod is intentionally not included in my modpack [Subtle Polish: A Collection of Fixes and Enhancements](https://steamcommunity.com/sharedfiles/filedetails/?id=2522974089) because it contains a significant gameplay change.  It is otherwise fully compatible.

### When to Install

This mod can be added before or during a game.  The new rules for allowing multiple "ascension path" ascension perks will take effect immediately, even for empires which have already chosen an ascension path. It is not recommended to remove during a game, as it could cause problems that have selected multiple ascension perks which are incompatible without this mod.  Always back up your savegame before trying to remove a mod.

### Required Mod Dependencies

[Deassimilate Machines](https://steamcommunity.com/sharedfiles/filedetails/?id=2553812372) contains all the changes to the Assimilation citizenship type as assimilation process required to support multiple assimilation types in one empire.

### Recommended Companion Mods

* [Leader Traits: All Eligible Species Traits](https://steamcommunity.com/sharedfiles/filedetails/?id=2499031295) will ensure that your leaders gain all applicable leader traits for any species traits their species possesses (such as Psionic, Cybernetic, and/or Erudite)
* [Psionic Ascension: Even in Other Empires](https://steamcommunity.com/sharedfiles/filedetails/?id=2601239912) grans the Latent Psionic and Psionic traits to all members of a species (galaxy-wide) when their founding empire chooses Psionic ascension; works with this mod to allow cybernetic Pops to also gain psionic powers
* [Retain Leaders from Integrated Subjects](https://steamcommunity.com/sharedfiles/filedetails/?id=2553818684) allows you to retain leaders from integrated subjects and conquered/infiltrated primitives; works with this mod so retained leaders can have multiple assimilations applied to them

### Known Issues

This mod overrides seven ascension perks from the base game.  Expect to see seven lines in error.log like this:

```

```

## Changelog

* 1.0.0 Initial version

## Source Code

Hosted on [GitHub](https://github.com/corsairmarks/assimilate_all_the_pops)

### Development Notes

It is best to clone this repository into `<Stellaris User's Directory>/Paradox Interactive/Stellaris/mod`, and then make a connection to the `mod` folder via a `*.mod` file's `path` property.  That will ensure the game can see the files, and also that CWTools will parse them.  Also note that the README.md file exists in the `mod` directory but is symbolically linked in the root directory.