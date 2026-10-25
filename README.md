# Nozavolochen (/ˌnəʊzəvəˈlɒtʃɛn/, "convergence")

One `xinput9_1_0.dll` hosts any number of independent spec-driven
runtime mods for No Man's Sky. Each mod is a folder with a
`mod.toml` describing pattern patches the loader applies at game
boot.

**Docs**: https://nozavolochen.github.io/docs/

## Mod distribution

The framework ships as its own [release](https://www.nexusmods.com/games/nomanssky/mods/4700?tab=files): an archive with
flat `xinput9_1_0.dll` at the root, marked as a required dependency on Nexus by your mod.

- **Vortex:** install with no extra steps. It routes the DLL into `Binaries/` for you.
- **Amethyst (Routing Rule, one-time):** Data tab > Routing Rules (bottom, near Search) > Add > Destinations: `Binaries`, Extensions: `.dll` > Save, then deploy.
- **Manual install (no manager):** drop `xinput9_1_0.dll` into the game's `Binaries/` folder.

Mods ship only their `mod.toml` (plus static files if required) and never bundle
the DLL.

## Build

```sh
make loader   # cross-build xinput9_1_0.dll (mingw on Linux)
```
