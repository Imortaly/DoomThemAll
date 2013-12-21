# DoomThemAll

DoomThemAll is a Minecraft (Bukkit) Mini-Game: Eliminate the other team using a Shotgun and Grenades!  
**Herzlich Willkommen, liebe "[Schlag den YouTuber](http://www.youtube.com/watch?v=exd8DE0fWHQ)"-Zuschauer!**

**Source-Code will follow soon!**

## How To Play
After joining a match you see a countdown above your inventory and you are allowed to investigate the map.  
At the beginning you join the red or the blue team and get a blazerod (Shotgun) and a snowball (Grenade). Both can be used with an right-click. While you can use the shotgun almoste every time, you have to kill somebody from the other team to get a new grenade.  
After one team reached 25 points the game is over.

## Setup
Follow these steps to setup and configure "DoomThemAll" on your server:

1. Download the plugin: Grab the current release from [here](https://github.com/MarvinMenzerath/DoomThemAll/releases) and put it in your plugins-folder.
2. Download Multiverse: Grab the current release from [here](http://dev.bukkit.org/bukkit-plugins/multiverse-core/) and put it in your plugins-folder.
3. Upload the maps: Upload the maps you want to play on and name them <code>dta-wX</code>, where "X" has to be a uniqe number. This will be the id of the arena. Example: <code>dta-w1</code>
4. Now start your server and import the worlds. Example: <code>/mv import dta-w1 normal -g flat</code>  After you did this for every arena, edit the multiverse-world-config and change the following parameters (if you want to):
  * <code>allowweather: false</code>
  * <code>difficulty: PEACEFUL</code>
  * <code>animals:
      spawn: false</code>
  * <code>monsters:
      spawn: false</code>
  * <code>hunger: false</code>
  * <code>gamemode: ADVENTURE</code>
5. Reload the Multiverse-Config: <code>/mv reload</code>
6. Configure the first arena:
  1. Teleport there: <code>/mv tp dta-w1</code>
  2. Now set every spawn (max 6!): Go to the place you want the players to spawn and type in <code>/dta setspawn [MAP] [SPAWN]</code>. Example: <code>/dta setspawn 1 1</code>
  3. Enable the arena: <code>/dta setmaxarena 1</code>.
  4. Set a lobby-spawn: <code>/dta setlobby</code>
  5. Place a sign to join the arena (every new line represents a line of the sign):
    1. <code>DoomThemAll</code>
    2. <code></code>
    3. <code>dta join [MAP-ID]</code>
    4. <code>[MAP-NAME]</code>

## Commands

### User
* Teleport to the lobby: <code>/dta lobby</code>
* Join an arena: <code>/dta join [MAP-ID]</code>
* Leave an arena: <code>/dta leave</code>

### VIP / Premium / YouTuber / ...
You have to use permissions to allow access to these commands
* Start the current arena (10 sec countdown): <code>/dta start</code>

### Admin / OP
* Set lobby-spawn: <code>/dta setLobby</code>
* Set map-spawn: <code>/dta setSpawn [MAP] [SPAWN]</code>
* Set maximum score: <code>/dta setMaxScore [SCORE]</code>
* Set maximum arena: <code>/dta setMaxArena [MAX]</code>

## Permissions
If you use a permissions-plugin like PermissionsEx, you'll probably want to restrict access to certain features of DoomThemAll:
* <code>doomthemall.premium</code>: Player is able to join full games and use its Shotgun faster than the other players
* more will follow soon!

## Notes:
* Currently the main-world (which contains the signs) has to be named <code>world</code>. This issue will be fixed very soon.

## FAQ
**Q**: I can not kill somebody from my team!  
**A**: This is the intended behaviour. Nobody wants assholes!

**Q**: I don't get any grenades!  
**A**: You have to kill somebody to get a new grenade.

**Q**: There are so many error-messages in the chat!  
**A**: Probably you removed a join-sign. Add it again to get rid of these messages.

## License
Copyright (C) 2013 [Marvin Menzerath](http://marvin-menzerath.de).

This program is free software; you can redistribute it and/or modify it under the terms of the GNU General Public License as published by the Free Software Foundation; either version 2 of the License, or (at your option) any later version.

This program is distributed in the hope that it will be useful, but WITHOUT ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the [GNU General Public License](https://github.com/MarvinMenzerath/InfoSphereApp/blob/master/LICENSE) for more details.
