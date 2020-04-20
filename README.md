This repository contains config files to set up an easy-to-use CSGO-server quickly that does not use SourceMod, but rcon only.

GOTV will be enabled, which takes up one slot on the server, so you need at least 11 slots. Alternatively, you can set `tv_enable 0`
in `server.cfg`, but you won't be able to record demos then.

# Usage

Open console and enter `rcon_password [yourpassword]` to log in.

Type `rcon cmds` for an overview of the commands.

If there are only two spectator slots (bug): To spectate one player: disable respawns, 2 join spectator, others join one team and type 'kill' .

A demo will be automatically recorded to a file named `_demo_latest.dem` .

>>> The server will override this file every time live.cfg is executed!

You can also record demos manually with `rcon tv_record [demoname]`. In this case the server will not override `_demo_latest.dem`.
You also have to type in `rcon tv_stoprecord` when the match is over. Otherwise the server will keep recording until the map changes (`changelevel`).

Pausing the match is also done manually with `rcon mp_pause_match` and `rcon mp_unpause_match`. You should bind `mp_pause_match` to a key.

# Commands

Available commands (rcon): 

* `warmup` (load warmup config [60.000$] and restart game)
* `prac` (load practice [cheats] config and restart game)
* `dryrun` (practice config [cheats], no respawns and restart game)
* `knife` (load kniferound config and restart game [need to swap teams manually])
* `live` (load 5v5 config and restart game)
* `rr` (restart game)
* `swap` (swap teams and restart game)
* `respawns` (toggles respawns on/off)
* `nobots` (kick bots)
* `impacts` (toggle bullet impacts)
* `playout` (don't end the game when a team reaches 16 points)
* `cmds` (shows commands)

# Installation

1. Download the latest [release](https://github.com/Linus4/csgo_config_rcon/releases).
1. Extract it in your `csgo` directory.
2. Fill in the fields marked with `FIXME` in `server.cfg`.
3. Restart CSGO-server.
