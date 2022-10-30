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
-   WarmupTimeLimit Integer *Minutes: amount of time before the mission starts* 
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
