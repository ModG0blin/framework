# Nozavolochen (/ˌnəʊzəvəˈlɒtʃɛn/, "convergence")

One `xinput9_1_0.dll` hosts any number of independent spec-driven
runtime mods for No Man's Sky. Each mod is a folder with a
`mod.toml` describing pattern patches the loader applies at game
boot.

**Docs**: https://nozavolochen.github.io/docs/

## Mod distribution

The framework ships as its own [release](https://www.nexusmods.com/games/nomanssky/mods/4700?tab=files): an archive with
flat `xinput9_1_0.dll` at the root, marked as a required dependency on Nexus by your mod. Vortex routes it into `Binaries/` with no extra steps; Amethyst needs a one-time Routing Rule (Data tab > Routing Rules: Destinations `Binaries`, Extensions `.dll`) or a manual move into `Binaries/`. Mods
ship only their `mod.toml` (plus static files if required) and never bundle
the DLL.

## Build

```sh
make loader   # cross-build xinput9_1_0.dll (mingw on Linux)
```
