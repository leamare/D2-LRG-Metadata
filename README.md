# Dota 2 Metadata

This repository contains metadata used by LRG-based projects.

Part of the data is managed manually.

## Legend

- `clusters` - Server-Region pairs
- `regions` - Regions list
- `regions_detailed` - Detailed regions list (multiple China regions and more specific location for regions)
- `creeps` - Creeps types with unit names
- `heroes` - Detailed heroes information
    - includes `released` field which is an array of `[unix timestamp, patchid, (optional) is CM/removed]` release date/addition to captain's mode
    - last flag is unset when the hero is added, 1 if added to CM, 0 if removed from CM
- `heroes_spells` - lists of hero abilities (QWEDFR in order) with their "mask" overrides and types
- `items` - Item IDs and tags
- `item_categories` - types of items
- `items_full` - full items data from Valve WebAPI
- `modes` - Game modes
- `patchdates` - Timestamps for gameplay versions
    - IDs are in OpenDota compatible format
    - starting with 6.70 (including versions which were not technically released in Dota 2, using early timestamps based on Stratz)
    - `main` key represents the release date for the original patch (without a letter), `add` is for "a" version of it
    - UNIX timestamps in `dates` array represent all other versions starting with litera "b"
- `versions` - Major version codes
- `zones` - Map zones
- `levels` - exp required for levels
- `overrides` - data overrides for many different types of metadata depending on the patch
    - doen't include all the matches and all the overwritable data (it would be too much otherwise)
    - only has a handful of patches
    - meant to describe changes to every patch below stated (e.g. item being placed in a different category)
- `spells_tags` - map of IDs and internal spell tags
- `spells_linked` - map of subabilities and their corresponding primary spells
- `heroes_spells` - objects describing abilities of heroes (using spell tags) and talents

## Map zones

Map zones are divided by polygons and described by verticies coordinates in cell format. So, for example, point [0,0] corresponds to cell [128,128] which belongs to the `dire_mid` polygon. Every polygon contains every point inside of it and on its perimeter.
