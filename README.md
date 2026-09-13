RadarHider

A CounterStrikeSharp plugin for CS2 dedicated servers that hides the radar when a player dies and restores it when they respawn.

What It Does:

When a player dies, their radar is disabled. When they respawn, it's re-enabled. This creates a more immersive spectator experience — dead players can't use the radar to track enemy positions while waiting to respawn.

This is useful for:
- Practice servers — forces dead players to rely on teammate comms instead of the radar
- Scrims / 10-mans — Removes the ability to see enemy positions if u aren't running plugins like Matchzy
- 2v5 / bot matches — prevents dead players from gaining free information

How It Works:

The plugin hooks into two CS2 game events:

| Event |                                Action                                 |
|-------|-----------------------------------------------------------------------|
| `player_death` | Sends `sv_disable_radar 1` to the dead player's client |
| `player_spawn` | Sends `sv_disable_radar 0` to the respawning player's client |

Requirements

- CS2 dedicated server (Windows or Linux)
- Metamod:Source 2.0 — [download here](https://www.metamodsource.net/downloads.php?branch=dev)
- CounterStrikeSharp — [download here](https://github.com/roflmuffin/CounterStrikeSharp/releases)

> Note: This plugin will not work on Valve official matchmaking (Premier, Competitive, Casual). It requires a community or dedicated server running Metamod:Source and CounterStrikeSharp.

Installation:

Step 1: Install Metamod:Source

1. Download the latest **Metamod:Source 2.0** build for your server's OS.
2. Extract the contents into your server's `game/csgo/` folder.
3. Add `-metamod` to your server's launch options (if not already present).
4. Start the server and run `meta list` in the console. You should see Metamod listed.

Step 2: Install CounterStrikeSharp

1. Download the latest **CounterStrikeSharp** release (use the `with-runtime` build for your first install).
2. Extract the contents into your server's `game/csgo/` folder.
3. Restart the server and run `meta list` again. You should now see both `Metamod:Source` and `CounterStrikeSharp`.

Step 3: Install RadarHider

1. Download the latest release from the [Releases page](../../releases).
2. Extract the ZIP into your server's `game/csgo/addons/counterstrikesharp/plugins/` folder.
3. Your final folder structure should look like this:
