# KadettNPSCompat

KadettNPSCompat is an unofficial GPL-3.0 modification of NetworkPerformanceSystem 1.14.0 for Valheim servers that use ServerManager.

It is not affiliated with or endorsed by MidnightsFX or the MidnightMods Thunderstore team.

## Changes from upstream

- Uses its own plugin ID, `Kadet_ttTeam.KadettNPSCompat`, its own DLL name, and its own BepInEx configuration and monitoring paths.
- Disables every NPS player-limit, admission, Steam-listing, and PlayFab lobby-capacity patch.
- Leaves player capacity and admission to ServerManager, avoiding the `ZNet.RPC_PeerInfo` patch conflict.
- Retains the other NPS networking mechanisms.

Modified source files carry dated modification notices.

## Build

The project targets .NET Framework 4.8 and restores JotunnLib through NuGet. Set `VALHEIM_INSTALL` to a compatible Valheim installation and `BEPINEX_PATH` to a compatible BepInEx installation, as described in `Environment.props.example`, then build `NetworkPerformanceSystem/NetworkPerformanceSystem.csproj` in Release mode.

No Valheim game assemblies are redistributed in this repository.

## License and credits

KadettNPSCompat is licensed under GPL-3.0; see [LICENSE](LICENSE).

Original NetworkPerformanceSystem was created by [MidnightsFX](https://github.com/MidnightsFX) and published on Thunderstore by [MidnightMods](https://thunderstore.io/c/valheim/p/MidnightMods/NetworkPerformanceSystem/).

Upstream source: https://github.com/MidnightsFX/Valheim-Network-Performance-System
