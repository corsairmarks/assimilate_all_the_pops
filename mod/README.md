# Overview

Do you want to assimilate all your Pops in all the ways? Then this mod is for you!

Regular empires can select any or all of: Synthetic Evolution, The Flesh is Weak, Mind Over Matter, and Engineered Evolution. Driven Assimilator machine empires can select either or both: Organo-Machine Interfacing and Synthetic Age. Hive-minded empires can select either or both: Organo-Machine Interfacing and Engineered Evolution.

You'll have all the corresponding assimilation types available to your empire, but they must be applied one-at-a-time.

# Changes

Allows regular empires to select Synthetic Evolution, The Flesh is Weak, Mind Over Matter, and/or Engineered Evolution. Allows Driven Assimilator machine empires to select both Organo-Machine Interfacing and Synthetic Age. Allows hive-minded empires to select both Organo-Machine Interfacing and Engineered Evolution. Also allows selecting the relevant ascension path traditions in combination with one-another.

Disables the "remove psionic" and "remove cybernetic" versions of the assimilation living standards. The game objects still exist, but they are no longer allowed for use (and the game should switch ongoing assimilations to the non-trait-specific version due to weight changes).

Psionic traits are still incompatible with hive minds, as in the unmodded game.

## Compatibility

Built for Stellaris version 3.7 "Canis Minor." Not compatible with achievements.

This mod overrides the seven ascension path-related ascension perks. It is generally not compatible with other mods that alter Synthetic Evolution, Synthetic Age, The Flesh is Weak, Organo-Machine Interfacing (both versions), Mind Over Matter, and Engineered Evolution. However, this mod features native support for [Planetary Diversity - Shroud Worlds](https://steamcommunity.com/sharedfiles/filedetails/?id=1960179456) and [Planetary Diversity - Unique Worlds](https://steamcommunity.com/sharedfiles/filedetails/?id=1740165239).

This mod is also not compatible with mods that adjust the Synthetics, Cybernetics, Psionics, or Genetics tradition categories (changes to individual tradition choices are compatible). Note that is you are playing Origin: The Children of Unit 04 from Planetary Diversity - Unique Worlds, be sure to choose the Bio-Synthetics tradition group before selecting any of the assimilation-related tradition groups (you do not need to finish the group, just unlocking it first is sufficient).

Also overridden are some events and other game code related to implementing assimilation:

* Event `action.64` - assimilation setup event, altered to ue triggers and effects (which themselves simply the game logic)
* Event `action.65` - main assimilation event, altered to use less duplicate code and pass two variables to its effect calls - the current number of assimilated Pops and the total number allowed for the year
* Event `utopia.2551` - Synthetic Evolution, altered to not change synthetic leaders of other species into the empire's main species (cyborgs are still fair game, however) and attempt to create an initial synthetic species with similar traits to the previous, organic species
* Effect `assimilation_effect` - main assimilation logic (called by `action.65`), altered so that deassimilated machines are not converted into the synthetic species for fully synthetic empires, also code de-duped
* Citizenship `citizenship_assimilation` - Assimilation, improved to understand that empires can have multiple assimilation types available

Do you want this mod to be compatible with your favorite "more tradition slots" mod? Simply override the scripted variable `assimilate_all_the_pops_tradition_categories_max` and set it equal to the maximum number of tradition slots allowed by your other mod. Ascension perk tradition slot checks (i.e. "Requires an empty Tradition Tree slot.") in this mod will use that number.

### When to Install

This mod can be added before or during a game. The new rules for allowing multiple "ascension path" ascension perks will take effect immediately, even for empires which have already chosen an ascension path. It is not recommended to remove during a game, as it could cause problems that have selected multiple ascension perks which are incompatible without this mod. Always back up your savegame before trying to remove a mod.

### Not Included in "Subtle Polish"

This mod is intentionally not included in my modpack [Subtle Polish: A Collection of Fixes and Enhancements](https://steamcommunity.com/sharedfiles/filedetails/?id=2522974089) because it contains a significant gameplay change. It is otherwise fully compatible.

### Required Mod Dependencies

* [Psionic Ascension: Even in Other Empires](https://steamcommunity.com/sharedfiles/filedetails/?id=2601239912) grants the Latent Psionic and Psionic traits to all members of a species (galaxy-wide) when their founding empire chooses Psionic ascension; works with this mod to allow cybernetic Pops to also gain psionic powers
* [Leader Traits: All Eligible Species Traits](https://steamcommunity.com/sharedfiles/filedetails/?id=2499031295) ensures that your leaders gain all applicable leader traits for any species traits their species possesses (such as Psionic, Cybernetic, and/or Erudite)

### Recommended Companion Mods

* [Civic: Organic Zealots](https://steamcommunity.com/sharedfiles/filedetails/?id=2920668465) provides a brand-new homicidal civic that can interfere with cybernetic and synthetic assimilation, and all empires can now choose to remove cybernetic implants via a deassimilation process (with the right technologies)
* [Deassimilate Machines](https://steamcommunity.com/sharedfiles/filedetails/?id=2553812372) allows regular (non-hive) empires to deassimilate machines into robots
* [Retain Leaders from Integrated Subjects](https://steamcommunity.com/sharedfiles/filedetails/?id=2553818684) allows you to retain leaders from integrated subjects and conquered/infiltrated primitives; works with this mod so retained leaders can have multiple assimilations applied to them

## Known Issues

This mod overrides one effect, one trigger, one species right, ten living standards, four events, and seven ascension perks from the base game. Expect to see 24 lines in error.log like these:

```
[04:00:32][game_singleobjectdatabase.h:165]: Object with key: can_harvest_dna already exists, using the one at  file: common/scripted_triggers/10_assimilate_all_the_pops_scripted_trigger_overrides.txt line: 6
[04:00:32][game_singleobjectdatabase.h:165]: Object with key: assimilation_effect already exists, using the one at  file: common/scripted_effects/00_scripted_effects.txt line: 4978
[04:00:32][game_singleobjectdatabase.h:165]: Object with key: citizenship_assimilation already exists, using the one at  file: common/species_rights/citizenship_types/30_assimilate_all_the_pops_citizenship_type_overrides.txt line: 7
[04:00:32][game_singleobjectdatabase.h:165]: Object with key: living_standard_deassimilation already exists, using the one at  file: common/species_rights/living_standards/20_assimilate_all_the_pops_living_standard_overrides.txt line: 12
[04:00:32][game_singleobjectdatabase.h:165]: Object with key: living_standard_ego_assimilation already exists, using the one at  file: common/species_rights/living_standards/20_assimilate_all_the_pops_living_standard_overrides.txt line: 45
[04:00:32][game_singleobjectdatabase.h:165]: Object with key: living_standard_ego_assimilation_psionic already exists, using the one at  file: common/species_rights/living_standards/20_assimilate_all_the_pops_living_standard_overrides.txt line: 90
[04:00:32][game_singleobjectdatabase.h:165]: Object with key: living_standard_cyborg_ego_assimilation already exists, using the one at  file: common/species_rights/living_standards/20_assimilate_all_the_pops_living_standard_overrides.txt line: 136
[04:00:32][game_singleobjectdatabase.h:165]: Object with key: living_standard_cyborg_ego_assimilation_psionic already exists, using the one at  file: common/species_rights/living_standards/20_assimilate_all_the_pops_living_standard_overrides.txt line: 220
[04:00:32][game_singleobjectdatabase.h:165]: Object with key: living_standard_tech_assimilation already exists, using the one at  file: common/species_rights/living_standards/20_assimilate_all_the_pops_living_standard_overrides.txt line: 258
[04:00:32][game_singleobjectdatabase.h:165]: Object with key: living_standard_cyborg_assimilation already exists, using the one at  file: common/species_rights/living_standards/20_assimilate_all_the_pops_living_standard_overrides.txt line: 331
[04:00:32][game_singleobjectdatabase.h:165]: Object with key: living_standard_cyborg_assimilation_psionic already exists, using the one at  file: common/species_rights/living_standards/20_assimilate_all_the_pops_living_standard_overrides.txt line: 393
[04:00:32][game_singleobjectdatabase.h:165]: Object with key: living_standard_psi_assimilation already exists, using the one at  file: common/species_rights/living_standards/20_assimilate_all_the_pops_living_standard_overrides.txt line: 423
[04:00:32][game_singleobjectdatabase.h:165]: Object with key: living_standard_psi_assimilation_cyborg already exists, using the one at  file: common/species_rights/living_standards/20_assimilate_all_the_pops_living_standard_overrides.txt line: 461
[04:00:34][eventmanager.cpp:368]: an event with id [action.64] already exists!  file: events/on_action_events_1.txt line: 7950
[04:00:34][eventmanager.cpp:368]: an event with id [action.65] already exists!  file: events/on_action_events_1.txt line: 8187
[04:00:34][eventmanager.cpp:368]: an event with id [utopia.2501] already exists!  file: events/utopia_on_action_events.txt line: 250
[04:00:34][eventmanager.cpp:368]: an event with id [utopia.2551] already exists!  file: events/utopia_on_action_events.txt line: 825
[04:00:36][game_singleobjectdatabase.h:165]: Object with key: ap_engineered_evolution already exists, using the one at  file: common/ascension_perks/assimilate_all_the_pops_ascension_path_overrides.txt line: 2
[04:00:36][game_singleobjectdatabase.h:165]: Object with key: ap_the_flesh_is_weak already exists, using the one at  file: common/ascension_perks/assimilate_all_the_pops_ascension_path_overrides.txt line: 50
[04:00:36][game_singleobjectdatabase.h:165]: Object with key: ap_organo_machine_interfacing already exists, using the one at  file: common/ascension_perks/assimilate_all_the_pops_ascension_path_overrides.txt line: 107
[04:00:36][game_singleobjectdatabase.h:165]: Object with key: ap_organo_machine_interfacing_assimilator already exists, using the one at  file: common/ascension_perks/assimilate_all_the_pops_ascension_path_overrides.txt line: 160
[04:00:36][game_singleobjectdatabase.h:165]: Object with key: ap_synthetic_evolution already exists, using the one at  file: common/ascension_perks/assimilate_all_the_pops_ascension_path_overrides.txt line: 197
[04:00:36][game_singleobjectdatabase.h:165]: Object with key: ap_mind_over_matter already exists, using the one at  file: common/ascension_perks/assimilate_all_the_pops_ascension_path_overrides.txt line: 295
[04:00:36][game_singleobjectdatabase.h:165]: Object with key: ap_synthetic_age already exists, using the one at  file: common/ascension_perks/assimilate_all_the_pops_ascension_path_overrides.txt line: 340
```

## Changelog

* 1.0.0 Initial version
* 2.0.0 Add support for Civic: Organic Zealots
    * Add a compatibility trigger for other mods to check whether this one is active
    * Consume the compatibility trigger from Civic: Organic Zealots
    * Remove old compatibility global flag
* 2.0.1 Disallow "The Flesh is Weak" from being chosen multiple times
* 3.0.0 Remove dependency on Deassimilate Machines
    * Assimilation overhaul now lives in this mod
    * Use triggers and effects from Civic: Organic Zealots, when it is also active
    * Use triggers and effects from Deassimilate Machines, when it is also active
    * Add compatibility for [Planetary Diversity - Shroud Worlds](https://steamcommunity.com/sharedfiles/filedetails/?id=1960179456) and [Planetary Diversity - Unique Worlds](https://steamcommunity.com/sharedfiles/filedetails/?id=1740165239)
* 3.0.1 Bugfixes from 3.0.0 overhaul
    * Properly allow cybernetic and synthetic assimilation when Civic: Organic Zealots is not active
    * Ensure that completing the Flesh Is Weak special project does not create two templates for your main species, and that it properly combines with Latent Psionic/Psionic of those traits were gained at approximately the same time
    * Fix compatibility with Planetary Diversity - Unique Worlds (was barring Bio-Synthetics from any assimilation, when instead they are allowed to have access to all types)
* 3.1.0 Allow empires that take a non-Genetics ascension, Driven Assimilators, and Rogue Servitors to harvest genetic material - thanks [wagnerleung0079](https://steamcommunity.com/profiles/76561198261183621) for reporting this game restriction
* 3.1.1 Bugfixes: reduce error logs, ensure dummy origin is not playable
* 4.0.0 Update for Stellaris version 3.7 "Canis Minor" - integrate underlying game changes

## Source Code

Hosted on [GitHub](https://github.com/corsairmarks/assimilate_all_the_pops)

### Development Notes

It is best to clone this repository into `<Stellaris User's Directory>/Paradox Interactive/Stellaris/mod`, and then make a connection to the `mod` folder via a `*.mod` file's `path` property. That will ensure the game can see the files, and also that CWTools will parse them. Also note that the README.md file exists in the `mod` directory but is symbolically linked in the root directory.