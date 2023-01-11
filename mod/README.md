# Overview

Do you want to assimilate all your Pops in all the ways? Then this mod is for you!

Regular empires can select any or all of: Synthetic Evolution, The Flesh is Weak, Mind Over Matter, and Engineered Evolution. Driven Assimilator machine empires can select either or both: Organo-Machine Interfacing and Synthetic Age. Hive-minded empires can select either or both: Organo-Machine Interfacing and Engineered Evolution.

You'll have all the corresponding assimilation types available to your empire, but they must be applied one-at-a-time.

# Changes

Allows regular empires to select Synthetic Evolution, The Flesh is Weak, Mind Over Matter, and/or Engineered Evolution. Allows Driven Assimilator machine empires to select both Organo-Machine Interfacing and Synthetic Age. Allows hive-minded empires to select both Organo-Machine Interfacing and Engineered Evolution. Also allows selecting the relevant ascension path traditions in combination with one-another.

Disables the "remove psionic" and "remove cybernetic" versions of the assimilation living standards. The game objects still exist, but they are no longer allowed for use (and the game should switch ongoing assimilations to the non-trait-specific version due to weight changes).

Psionic traits are still incompatible with hive minds, as in the unmodded game.

## Compatibility

This mod overrides the seven ascension path-related ascension perks. It is not compatible with other mods that alter Synthetic Evolution, Synthetic Age, The Flesh is Weak, Organo-Machine Interfacing (both versions), Mind Over Matter, and Engineered Evolution. It is also not compatible with mods that adjust the Synthetics, Cybernetics, Psionics, or Genetics tradition categories (changes to individual tradition choices are compatible).

Built for Stellaris version 3.6 "Orion." Not compatible with achievements.

Do you want this mod to be compatible with your favorite "more tradition slots" mod? Simply override the scripted variable `assimilate_all_the_pops_tradition_categories_max` and set it equal to the maximum number of tradition slots allowed by your other mod. Ascension perk tradition slot checks (i.e. "Requires an empty Tradition Tree slot.") in this mod will use that number.

### When to Install

This mod can be added before or during a game. The new rules for allowing multiple "ascension path" ascension perks will take effect immediately, even for empires which have already chosen an ascension path. It is not recommended to remove during a game, as it could cause problems that have selected multiple ascension perks which are incompatible without this mod. Always back up your savegame before trying to remove a mod.

### Not Included in "Subtle Polish"

This mod is intentionally not included in my modpack [Subtle Polish: A Collection of Fixes and Enhancements](https://steamcommunity.com/sharedfiles/filedetails/?id=2522974089) because it contains a significant gameplay change. It is otherwise fully compatible.

### Required Mod Dependencies

* [Deassimilate Machines](https://steamcommunity.com/sharedfiles/filedetails/?id=2553812372) contains all the changes to the Assimilation citizenship type and assimilation process required to support multiple assimilation types in one empire
* [Psionic Ascension: Even in Other Empires](https://steamcommunity.com/sharedfiles/filedetails/?id=2601239912) grants the Latent Psionic and Psionic traits to all members of a species (galaxy-wide) when their founding empire chooses Psionic ascension; works with this mod to allow cybernetic Pops to also gain psionic powers
* [Leader Traits: All Eligible Species Traits](https://steamcommunity.com/sharedfiles/filedetails/?id=2499031295) ensures that your leaders gain all applicable leader traits for any species traits their species possesses (such as Psionic, Cybernetic, and/or Erudite)

### Recommended Companion Mods

* [Retain Leaders from Integrated Subjects](https://steamcommunity.com/sharedfiles/filedetails/?id=2553818684) allows you to retain leaders from integrated subjects and conquered/infiltrated primitives; works with this mod so retained leaders can have multiple assimilations applied to them

## Known Issues

This mod overrides one event, seven ascension perks, and ten living standards from the base game. Expect to see eighteen lines in error.log like this:

```
[08:19:32][game_singleobjectdatabase.h:165]: Object with key: living_standard_deassimilation already exists, using the one at file: common/species_rights/living_standards/10_assimilate_all_the_pops_living_standards.txt line: 9
[08:19:32][game_singleobjectdatabase.h:165]: Object with key: living_standard_ego_assimilation already exists, using the one at file: common/species_rights/living_standards/10_assimilate_all_the_pops_living_standards.txt line: 42
[08:19:32][game_singleobjectdatabase.h:165]: Object with key: living_standard_ego_assimilation_psionic already exists, using the one at file: common/species_rights/living_standards/10_assimilate_all_the_pops_living_standards.txt line: 92
[08:19:32][game_singleobjectdatabase.h:165]: Object with key: living_standard_cyborg_ego_assimilation already exists, using the one at file: common/species_rights/living_standards/10_assimilate_all_the_pops_living_standards.txt line: 130
[08:19:32][game_singleobjectdatabase.h:165]: Object with key: living_standard_cyborg_ego_assimilation_psionic already exists, using the one at file: common/species_rights/living_standards/10_assimilate_all_the_pops_living_standards.txt line: 187
[08:19:32][game_singleobjectdatabase.h:165]: Object with key: living_standard_tech_assimilation already exists, using the one at file: common/species_rights/living_standards/10_assimilate_all_the_pops_living_standards.txt line: 222
[08:19:32][game_singleobjectdatabase.h:165]: Object with key: living_standard_cyborg_assimilation already exists, using the one at file: common/species_rights/living_standards/10_assimilate_all_the_pops_living_standards.txt line: 270
[08:19:32][game_singleobjectdatabase.h:165]: Object with key: living_standard_cyborg_assimilation_psionic already exists, using the one at file: common/species_rights/living_standards/10_assimilate_all_the_pops_living_standards.txt line: 310
[08:19:32][game_singleobjectdatabase.h:165]: Object with key: living_standard_psi_assimilation already exists, using the one at file: common/species_rights/living_standards/10_assimilate_all_the_pops_living_standards.txt line: 340
[08:19:32][game_singleobjectdatabase.h:165]: Object with key: living_standard_psi_assimilation_cyborg already exists, using the one at file: common/species_rights/living_standards/10_assimilate_all_the_pops_living_standards.txt line: 377
[08:19:34][eventmanager.cpp:368]: an event with id [utopia.2501] already exists!  file: events/utopia_on_action_events.txt line: 250
[08:19:37][game_singleobjectdatabase.h:165]: Object with key: ap_engineered_evolution already exists, using the one at file: common/ascension_perks/assimilate_all_the_pops_ascension_path_overrides.txt line: 2
[08:19:37][game_singleobjectdatabase.h:165]: Object with key: ap_the_flesh_is_weak already exists, using the one at file: common/ascension_perks/assimilate_all_the_pops_ascension_path_overrides.txt line: 50
[08:19:37][game_singleobjectdatabase.h:165]: Object with key: ap_organo_machine_interfacing already exists, using the one at file: common/ascension_perks/assimilate_all_the_pops_ascension_path_overrides.txt line: 87
[08:19:37][game_singleobjectdatabase.h:165]: Object with key: ap_organo_machine_interfacing_assimilator already exists, using the one at file: common/ascension_perks/assimilate_all_the_pops_ascension_path_overrides.txt line: 121
[08:19:37][game_singleobjectdatabase.h:165]: Object with key: ap_synthetic_evolution already exists, using the one at file: common/ascension_perks/assimilate_all_the_pops_ascension_path_overrides.txt line: 158
[08:19:37][game_singleobjectdatabase.h:165]: Object with key: ap_mind_over_matter already exists, using the one at file: common/ascension_perks/assimilate_all_the_pops_ascension_path_overrides.txt line: 234
[08:19:37][game_singleobjectdatabase.h:165]: Object with key: ap_synthetic_age already exists, using the one at file: common/ascension_perks/assimilate_all_the_pops_ascension_path_overrides.txt line: 279
```

## Changelog

* 1.0.0 Initial version
* 2.0.0 Add support for Civic: Organic Zealots
    * Add a compatibility trigger for other mods to check whether this one is active
    * Consume the compatibility trigger from Civic: Organic Zealots
    * Remove old compatibility global flag

## Source Code

Hosted on [GitHub](https://github.com/corsairmarks/assimilate_all_the_pops)

### Development Notes

It is best to clone this repository into `<Stellaris User's Directory>/Paradox Interactive/Stellaris/mod`, and then make a connection to the `mod` folder via a `*.mod` file's `path` property. That will ensure the game can see the files, and also that CWTools will parse them. Also note that the README.md file exists in the `mod` directory but is symbolically linked in the root directory.