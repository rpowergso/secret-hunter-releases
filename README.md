# Secret Hunter

Secret Hunter is a multiplayer Minecraft Java Edition game mode for Paper servers. Runners race to defeat the Ender Dragon while one or more secretly assigned hunters try to eliminate them.

## Download

**[Download SecretHunter-1.0.14.jar](https://github.com/rpowergso/secret-hunter-releases/releases/download/v1.0.14/SecretHunter-1.0.14.jar)** · [Release notes and checksum](https://github.com/rpowergso/secret-hunter-releases/releases/tag/v1.0.14) · [All releases](https://github.com/rpowergso/secret-hunter-releases/releases)

The 1.0.14 beta targets **Minecraft Java Edition 26.3** on **Paper 26.3**. The server needs **Java 25 or newer** and at least **two players** to start a round. Players join with a matching Minecraft client. Paper is the only required server dependency.

## Install and start a round

1. Set up a dedicated [Paper server](https://docs.papermc.io/paper/getting-started/) and back up any existing server data.
2. Stop the server and place the downloaded JAR in its `plugins/` folder.
3. Start the server. The plugin creates `plugins/SecretHunter/config.yml`.
4. When at least two players are online, have a server operator run `/resethunt`, then `/starthunt 1` to start with one hunter.
5. For a fresh seed between rounds, run `/resethuntworld`, then prepare and start the next round. The plugin creates a new Overworld, Nether, and End and retains the previous world files.

## How to play

- **Runners** work together to defeat the Ender Dragon before the hunters eliminate them.
- **Hunters** use a tracker compass to cycle through living runners. It points to the selected runner in the same dimension or to their last known location in the hunter’s current dimension.
- **Players** can share coordinates, request help, and call an emergency meeting using chat commands.

## Server commands

The following commands require `secrethunter.admin`, which defaults to server operators.

| Command | What it does |
| --- | --- |
| `/resethunt` | Prepare the hunt and move online players to the starting area |
| `/starthunt [hunter-count]` | Assign roles and start the countdown |
| `/resethuntworld` | Create fresh hunt worlds with a new seed |
| `/secrethunterreload` | Reload the configuration |

During a hunt, players can use `/alert` to share their coordinates, `/emergency` to call a meeting at their location, `/lost` to ask for help, and `/shout <message>` to send an allowed global message. Use `/savecoord <name>`, `/savedcoordslist`, and `/retrievecoords <name>` to save and recall locations during the server session.

## Configuration

The configuration controls the number of hunters, countdown, world borders, tracking, player-list visibility, and loot. By default, preparing a round clears online players’ inventories. World resets retain previous world files, so repeated resets increase disk use.

## Feedback

For bug reports, include your Minecraft, Paper, and Java versions and the steps to reproduce the issue. [GitHub Issues](https://github.com/rpowergso/secret-hunter-releases/issues)

## Credits

Rafi Mintz (rpowergso) directed development and tested the plugin. Secret Hunter is an unofficial Minecraft project inspired by [zorato’s Secret Hunter series](https://www.youtube.com/watch?v=JaN_pfpr1tE).
