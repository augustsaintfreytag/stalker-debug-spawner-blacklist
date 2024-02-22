(Cover image pending)

# STALKER Debug Spawner Blacklist

A mod to remove a number of disabled items that by default appear in the Anomaly debug item spawner. Effectively cleans up the spawner interface to only show items that are actively used in the game and may be acquired in normal gameplay. Removes all items that either have no assigned localized name or no icon. Additionally removes the disabled toolkits made obsolete by Arti's *Streamlined Upgrades* mod.

## Approach

For intentionally disabled and obsoleted items, this mod modifies the existing spawner item blacklist `spawner_blacklist.ltx` with a DLTX patch. For the rest, there is a script module patching the item spawn table function of `ui_debug_launcher` to include a number of simple heuristics to detect and remove items that should not be spawned. Most of the records removed this way are added by mods with incorrect item `class` or `kind` properties (e.g. various weapon and sound dummies).

## License

This mod was created by Saint for free use by the STALKER modding community with basic attribution under the MIT license. This mod may be distributed with mod packs. Includes modules using DXML, created by Demonized (https://github.com/themrdemonized).