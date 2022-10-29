Documentation for v.1.0.0. Currently, mostly, a pastebin for my own notes as the TW documentation is not comprehensive enough. 

# Acknowledgements 
- Mount & Blade Modding (Discord: https://discord.gg/92uJp7YD2u) 
- Byako 
- Muz 

# Hosting Bannerlord Dedicated Servers

## Hosting a Server on Windows 
I'd strongly recommend following the guide created by That Horns Guy [here](https://youtu.be/9Hvuz12Bfzg), especially if this is your first time hosting a server. 

## Hosting a Server on Linux 
TW has not provided support for Dedicated Server hosting on Linux OS, however there is a community solution [here](https://forums.taleworlds.com/index.php?threads/guide-dedicated-server-on-linux.454799/).

## Bugs / Warnings
- A list of current bugs / warnings with hosting a dedicated server can be found [here](https://forums.taleworlds.com/index.php?threads/hosting-a-dedicated-server-back-end-problems.454786).

## Server Configurations
-   ServerName String *this is the name of the server, which will be
    displayed in the server lobby*
-   GamePassword String *optional: password lock your server, put in a
    password here*
-   GameType String *this is the type of game type, e.g., Duel, Battle,
    Captain..*
-   Map String *this is the map you will host first, take a look at*
    ***Maps*** *to find the dictionary for the specific map file name*
-   CultureTeam1 *the culture for Team 1*, e.g., khuzait, aserai
-   CultureTeam2 *the culture for Team 2*, e.g., khuzait, aserai
-   AllowPollsToKickPlayers Boolean 
-   AllowPollsToBanPlayers Boolean
-   AllowPollsToChangeMaps Boolean
-   RespawnPeriodTeam1 
-   RespawnPeriodTeam2 
-   RoundPreparationTimeLimit 
-   MaxNumberOfPlayers Integer *the capped number of players that can join your server* 
-   AutoTeamBalanceThreshold Integer
-   FriendlyFireDamageMeleeFriendPercent Integer
-   FriendlyFireDamageMeleeSelfPercent Integer
-   FriendlyFireDamageRangedFriendPercent Integer 
-   FriendlyFireDamageRangedSelfPercent Integer
-   MinNumberOfPlayersForMatchStart Integer 
-   RoundTotal Integer *believe this is the number of missions that will be played before the game ends.* 
-   MapTimeLimit Integer *number of minutes your mission will last for on the map before ending (if score limit isn't reached)* 
-   RoundTimeLimit 
-   WarmupTimeLimit Integer *amount of time before the mission starts* 
-   SingleSpawn Boolean (True/False) not really sure what this is 
-   NumberOfBotsTeam1 Integer *this sets the number of bots on Team 1,
    this is immediate for TDM.*
-   NumberOfBotsTeam2 Integer *this sets the number of bots on Team 2,
    this is immediate for TDM.*
-   UnlimitedGold Boolean (True/False) *this sets whether gold is
    unlimited or not. Appears to work immediately for TDM without ending
    mission.* There are bugs associated with this, check the Bugs
    section.
-   end_game_after_mission_is_over Boolean (True/False) *end the server after the mission is over, do NOT enable if you want another map after the first map.* 
-   start_game_and_mission *start the server, start the mission - no arguments required.* 





### Terminology

-   Games are considered what is being hosted
-   Each game has a mission which is defined as the gametype, etc..
-   The game mode of Captain is called Sergeant in the game files.

### Specs Required for Server Hosting

-   Still not 100%, but I was using just over 1 GB memory RAM & capping
    at 20% of 32 GB cpu, 6.4GB with 400 bots

### Other Tips / Tricks

-   Default warmup for battle is 5 minutes, possibly extends to other
    game modes.
-   you can load in new missions without restarting the server by
    entering new\_mission.
-   Server will max out at around 300 bots.

then waiting until process is cleared, then entering in the new
mission.. note that this doesn’t apparently work to clear some
parameters, in which case you need to restart (e.g., warmup time changes
won’t be overridden from the initial mission).

You won’t be able to use TDM maps for battle due to spawns

Apparently duel works with battle (to a certain extent?)

Duel can’t be preset with a map (will error out, needs to be added to a
queue).



### Maps

The maps used for server hosting are not the same as their in-game
names, the following is a dictionary of the maps used for hosting with
their in-game names..

### Battle

-   mp\_battle\_map\_001 = Cypegos Blockage

### Captain/Sergeant

Captain is called Sergeant in game files.

-   mp\_sergeant\_map\_001 = broken map

-   mp\_sergeant\_map\_002 - 004 = maps don’t exist

-   mp\_sergeant\_map\_005 = no name, ruins in forest with bridge - does
    work

-   mp\_sergeant\_map\_006 = map doesn’t exist

-   mp\_sergeant\_map\_007 = Ruins of Jawwali

-   mp\_sergeant\_map\_008 = Druimmor Forest

-   mp\_sergeant\_map\_009 = Cliffs of Akkalat
    ![cliffs_of_akkalat](https://user-images.githubusercontent.com/116319794/198414621-2d2a2208-b213-4f74-ae20-c639ffae4e8a.jpg)

-   mp\_sergeant\_map\_010 = Pendaric
    ![pendaric](https://user-images.githubusercontent.com/116319794/198414680-82d48633-0387-4300-b390-964940174c46.jpg)

-   mp\_sergeant\_map\_011 = Isle of Deriad (raining map)

-   mp\_sergeant\_map\_011\_rw = Isle of Deriad, not sure what
    difference is

#### Hosting Custom Maps 
Will update soonish. 

#### Updating DedicatedServerHelper 
If there is an update to the game / DedicatedServerHelper you will need to manually update the XML of the DedicatedServerHelper module for your Dedicated Server. 

You can do this by going to the following directory: 
C:\Program Files (x86)\Steam\steamapps\common\Mount & Blade II Dedicated Server\Modules\DedicatedCustomServerHelper\SubModule.xml 

And changing the "Version value" to the version of the DedicatedServerHelper for when you launch the game. 

Note that these modules are not the correct version, the DedicatedServerHelper needs to be updated on the server side.. 
![image](https://user-images.githubusercontent.com/116319794/198408147-d9016975-061f-4e49-aabb-21010e945233.png) 
![image](https://user-images.githubusercontent.com/116319794/198408231-63339ef8-adc7-40be-a12c-ee6754e9c769.png)

Update the XML to match that of the game's current version. 
![image](https://user-images.githubusercontent.com/116319794/198408245-3bafc121-c61d-4d64-99b2-4ec238ecab6d.png)

#### Unable to find MultiplayerForcedAvatars
The solution to this issue is:

To copy the MultiplayerForcedAvatars from your Mount & Blade II game directory, e.g.,:
C:\Program Files (x86)\Steam\steamapps\common\Mount & Blade II Bannerlord\Modules\Native\MultiplayerForcedAvatars

And copy and paste those files to the following path:
'C:\Program Files (x86)\Steam\steamapps\common\Mount & Blade II Dedicated Server\Modules\Native\MultiplayerForcedAvatars'


### Maps 
#### Skirmish

mp\_skirmish\_map\_008\_skin = Port of Omar

#### Team Deathmatch

- mp\_tdm\_map\_001 = 

- mp\_tdm\_map\_001\_spring = 

- mp\_tdm\_map\_003 =
Tsagaan Castle
![mp_tdm_map_003](https://user-images.githubusercontent.com/116319794/198414710-0e7165cd-8634-4c0c-ab86-a0e3a73fdec6.jpg)

### Duel

mp\_duel\_001 = Imperial Villa, does not work as a duel map (cannot
accept duels).

## GameTypes
-   Duel
-   FreeForAll, this game mode doesn’t work.
-   Sergeant
-   Battle 
-   Skirmish 
-   TeamDeathmatch
