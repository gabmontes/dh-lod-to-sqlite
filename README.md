# Distant Horizons LOD to SQLite Conversion tool

[Distant Horizons 2.0.0 RC4](https://discord.com/channels/881614130614767666/881744029509906472/1164905424571617320) changes the way the LODs are stored, from `.lod` files to a SQLite database.
Since the LODs are not automatically converted (does not make sense), all data must be re-generated.
Really?

For those who have been beta-testing [Distant Horizons](https://www.curseforge.com/minecraft/mc-mods/distant-horizons) for a while, have a good amount of LOD already generated and don't feel like playing Minecraft the old fashion until all the LODs are generated again, this tool may help.

## Usage

```sh
npx https://github.com/gabmontes/dh-lod-to-sqlite <world data directory>
```

The data directory is where all the world data is stored, including the folders containing the LODs and `DistantHorizons.sqlite` files.
In macOS, those are usually at:

- Single player: `~/Library/Application\ Support/minecraft/saves/<world name>`
- Multiplayer: `~/Library/Application\ Support/minecraft/Distant_Horizons_server_data/<server name>`

### Note

The tool was developed and tested in macOS but it should work in Windows too.

## Acknowledgements

Thanks to [James Saibel](https://gitlab.com/jeseibel) and team for this awesome mod and support to code this tool.

And also thanks to [Renato Alencar](https://github.com/renatoalencar) and [Juanra GM](https://github.com/juanrgm) for [adding `BIGINT` support to `node-sqlite3` and making it easy to install the patched version](https://github.com/TryGhost/node-sqlite3/pull/1501#issuecomment-1160140213).
