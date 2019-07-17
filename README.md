# Dota 2 Metadata

This repository contains metadata used by LRG-based projects.

Part of the data is managed manually.

## Legend

- `clusters` - Server-Region pairs
- `regions` - Regions list
- `regions_detailed` - Detailed regions list (multiple China regions and more specific location for regions)
- `creeps` - Creeps types with unit names
- `heroes` - Detailed heroes information from Valve WebAPI
- `items` - Item IDs and tags
- `modes` - Game modes
- `patchdates` - Timestamps for lettered gameplay versions
- `versions` - Major version codes
- `zones` - Map zones

## Map zones

Map zones are divided by polygons and described by verticies coordinates in cell format. So, for example, point [0,0] corresponds to cell [128,128] which belongs to the `dire_mid` polygon. Every polygon contains every point inside of it and on its perimeter.
