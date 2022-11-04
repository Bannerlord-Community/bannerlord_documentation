#### Updating DedicatedServerHelper 
If there is an update to the game / DedicatedServerHelper you will need to manually update the XML of the DedicatedServerHelper module for your Dedicated Server, as this isn't automatically updated. 

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
