# Secret Hunter

Secret Hunter is an unofficial, server-side Minecraft Java Edition game mode inspired by [zorato’s Secret Hunter series](https://www.youtube.com/watch?v=JaN_pfpr1tE). One or more players are secretly assigned to hunt the runners before they defeat the Ender Dragon. Hunters can cycle their targets with a tracker compass. The compass points to the target in the same dimension or to the target’s last known position in the hunter’s current dimension.

## Compatibility

- Minecraft Java Edition 26.3
- Paper server 26.3. The plugin was compiled against Paper build 249.
- Java 25 or newer on the server. Players use a matching Minecraft client.
- At least two players. Paper is the only required server dependency.
- Server startup, world creation and fresh-seed reset were verified on Paper build 249 with Java 26. Multiplayer play and compass tracking are beta features awaiting a full multiplayer test.

## Installation

Get the JAR from the [GitHub beta release](https://github.com/rpowergso/secret-hunter-releases/releases/tag/v1.0.14).

1. Set up a dedicated [Paper server](https://docs.papermc.io/paper/getting-started/) and back up any existing server data.
2. Stop the server and place `SecretHunter-1.0.14.jar` in its `plugins/` folder.
3. Start the server. The plugin creates `plugins/SecretHunter/config.yml` with settings for the countdown, world border, tracking, chat and loot.
4. Have an operator run `/resethunt`, then `/starthunt 1` once at least two players are online.
5. Between rounds, run `/resethuntworld` for a new seed. This creates three new hunt dimensions. Previous world files are retained, so repeated resets will increase disk use.

The default configuration clears online players’ inventories when preparing a round. During active hunts the plugin also changes player-list visibility and chat behavior. Use a dedicated server for the game.

## Commands

| Command | Action |
| --- | --- |
| `/resethunt` | Prepare the current hunt and move online players to its starting area |
| `/starthunt [hunter-count]` | Assign roles and start the countdown |
| `/resethuntworld` | Create and verify fresh hunt worlds |
| `/secrethunterreload` | Reload configuration |
| `/shout <message>` | Broadcast a message during a hunt |
| `/alert`, `/emergency`, `/lost` | Share a location, call a meeting or request help |
| `/savecoord <name>`, `/savedcoordslist`, `/retrievecoords <name>` | Save and retrieve coordinates during the server session |

The first four commands require the `secrethunter.admin` permission, which defaults to operators.

## Credits

rpowergso directed development and tested the project. The plugin code was generated using AI. The game concept is inspired by [zorato’s Secret Hunter series](https://www.youtube.com/watch?v=JaN_pfpr1tE). Secret Hunter is an unofficial Minecraft project.
