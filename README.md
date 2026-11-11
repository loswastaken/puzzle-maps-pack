# Puzzle Maps pack

packwiz pack for Los's "Puzzle Maps" server: Minecraft 1.17.1, Forge 37.1.1, with the 46 server mods (Biomes O' Plenty, Alex's Mobs, Cyclic, Waystones, JEI, WorldEdit and more), byte-identical to the server's jars. Links only, no mod files.

Server: `dorkunify.duckdns.org:25565` (at home or on the VPN: `10.24.4.143:25565`). Whitelisted players only; send Los your Minecraft username first.

## Quick setup (one command)
Close Prism Launcher first.

Windows (PowerShell):

    irm https://raw.githubusercontent.com/loswastaken/puzzle-maps-pack/main/join.ps1 | iex

macOS / Linux:

    curl -fsSL https://raw.githubusercontent.com/loswastaken/puzzle-maps-pack/main/join.sh | bash

It installs Prism Launcher if needed, creates (or refreshes) the "Puzzle Maps" instance, sets up the mod sync and adds the server. Then open Prism, sign in with your Microsoft account, and press Play. Read `join.ps1` / `join.sh` first if you like; they only touch Prism's own folder.

## Hand downloads
- **Escape Rope 1.1.2** (required): no longer a hand download. Its old CurseForge page is gone (the author deprecated the mod and reused the project for Awesome Dungeon Ocean - NeoForge), so the pack now fetches the same file straight from CurseForge's CDN (file 3512824, sha1-checked) during the launch-time sync.
- **OptiFine 1.17.1 HD U H1** (optional, recommended): the script asks, opens https://optifine.net/adloadx?f=OptiFine_1.17.1_HD_U_H1.jar and picks it up from Downloads. OptiFine can't be linked in a pack, so it's never synced automatically.

## Manual setup
1. Create a Prism instance named "Puzzle Maps": Minecraft 1.17.1, Forge 37.1.1 (Java 17).
2. Download https://github.com/packwiz/packwiz-installer-bootstrap/releases/latest/download/packwiz-installer-bootstrap.jar into the instance's `.minecraft` folder.
3. Instance Settings > Custom commands > Pre-launch command:
   `"$INST_JAVA" -jar packwiz-installer-bootstrap.jar https://raw.githubusercontent.com/loswastaken/puzzle-maps-pack/main/pack.toml`
4. Launch. Mods sync on every launch.
