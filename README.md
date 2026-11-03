# NovaClient — Minecraft 1.21.1

A client-side Fabric starter mod with a Rimuru/Tempest-inspired icy-blue UI and HUD.

## Included
- Fabric client mod for Minecraft **1.21.1**, Java **21**
- Right Shift opens the Tempest settings screen
- V toggles sprint state (client-side sprint assist)
- C toggles a zoom indicator only (actual camera zoom is not implemented yet)
- FPS, CPS, keystrokes, coordinates, ping, armor, potion-effect and sprint HUD rows
- Settings saved to `config/nova-client.json`
- GitHub Actions workflow to build a JAR remotely

## Build
Upload the contents of this folder to the root of a GitHub repository, keeping `.github/workflows/build.yml`.
Open **Actions** → **Build NovaClient** → **Run workflow**. When complete, download the
`NovaClient-Minecraft-1.21.1` artifact. Put the resulting JAR in the `mods` folder of a
Minecraft 1.21.1 Fabric installation with Fabric API installed.

## Honest status
This is source code, not a prebuilt JAR. The GitHub workflow is provided but has not
been executed or verified in this environment. This is a Fabric mod, not a standalone
launcher. A custom animated Rimuru background, drag-and-drop HUD editor, minimap,
account authentication, cosmetics, and true camera zoom are not implemented in this
starter version. The UI uses an original blue Tempest-inspired style and does not
include copyrighted character artwork.

## Tempest visual update
- Adds a custom moonlit blue Tempest-style background to Minecraft screens that use the standard `Screen.renderBackground` method (including the NovaClient settings screen and title/menu screens).
- Adds a tiny original pixel-art Diablo-inspired mascot to vanilla `ButtonWidget` buttons.
- This is a client-side visual theme; it does not change gameplay or add cheats.

Build verification: not run in this environment because Gradle is not installed. Build with Java 21 using the included GitHub Actions workflow or a local Gradle installation.

## NovaBoost (experimental)
The NovaClient menu includes a NovaBoost toggle. When enabled, it lowers Minecraft's view distance to 6 chunks and simulation distance to 5 chunks. This can reduce CPU/GPU load on lower-end devices, but FPS gains vary by world and device. It does not change combat, movement, or other gameplay mechanics. The setting does not restore the previous distances automatically when disabled; adjust them in Minecraft Video Settings if needed.
