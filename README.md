## Goal: 
Shoot the zombies; don't die.

## How to Play

### Install
Download from my google drive: https://drive.google.com/file/d/1ESz5FVUZe8Ux3ZBdHZ8VucNXaHoZ_WwF/view?usp=drive_link
 (Due to the size of the game, I have stopped paying for additional storage on github, so the repo can no longer fit the game build. Downloading from my drive should be faster anyway)
Unzip repo
Double click exe
Play
If it doesn't automatically launch your VR software, maybe try doing that yourself. Don't be lazy.

### Controls:
* Movement is done with the left thumbstick. When you move, there is a blinder effect that happens to keep oli from getting motion sick. I will make this configurable in the options one day.

* Both snap turning and smooth turning are now available in the gameplay setting in the menu. The smooth turning rate is not configurable right now. You can also select manual turning if you prefer to actually turn yourself.

* Certain interactions are done by pressing the thumbstick buttons on either of the oculus style controllers (quest, newer vives, and index) on old school vive controllers it is pressing on the right button of the trackpad of either controller. Currently, this is only used to operate the random box. I also have some doors that work with it, but they are not currently in the game.

* Opening the menu is done with the B or Y buttons on either controller if no item is held in that hand. For older vive controllers it is down on the trackpad of either controller if no item is held. If an item is held, the menu button will be disabled and possibly used for other things. Once the menu is opened, point your hand at the menu to get the laser cursor to move and use the trigger to interact with it. Theoretically it auto applies and saves things by default once they are changed, so no need to hit those unless you uncheck the boxes. When you've had enough of the madness, press the menu button again to close it. I have seen a bug where certain gun interactions won't work after opening the menu with your dominant hand. Not quite sure why.

* Guns are picked up using the grip buttons of your controllers. Holding the grip is not required, and will actually be detrimental since the grip is released by pressing the grip button again. I will make this configurable in the future.

* Sometimes the foregrip hitboxes are wonky, so good luck with that. I also think one gun may drop from your secondary grip when you release the main grip because I just never got around to changing that setting. If you find out which one that is, let me know because I forget. In general though, all controls are done by the hand with the "main" grip. That is, the one with the finger on the trigger. If you pull the imaginary trigger on the forgrip of a gun, it does not fire (shocking, I know). The main grip hand can also be used to toggle firing modes on guns which support it and to reload the weapon.

* Toggling firing modes is done with the B/Y button depending on your controller type and which hand. For you weirdo vive users, it is Right on the trackpad. This is the same binding as the menu, so when holding a gun, you cannot open the menu with that hand. Deal with it.

* Reloading is currently set to the "easy" variant, which is just pressing a button. Only some of the guns I have are properly set up for full reloading mechanics, so for now, it is just a button press for everything. On modern controllers it is the X/A button depending on which hand and controller type. For the vive losers (for the love of god just upgrade already), it is Down on the trackpad.

* To use weapon attachments, grab them using the TRIGGER of an empty hand and continue holding the trigger as you place the attachment onto the weapon. The suppressor goes on the end, sights go in the sight place, the laser goes somewhere near the front of the barrel, and foregrips go where it makes sense. Attachments can be removed in the same manner. Occasionally attaching a sight will do a weird collision things and bump the player several feet then attach the sight sideways. Idk what's going on there. I'll look into it one day. It's not that common though. If it happens, just take it off and put it back on and never speak of the incident.

### Settings: 
* ~~The video settings exist, but don't do a whole lot. Nuking all the settings to low except shadows can save a tiny bit of vram with no major noticeable effects. The shadow quality has the biggest effect due to all of the fog, and should be kept at high or epic unless you want crappy fog. You don't want crappy fog.~~ I completely reworked the graphics and the settings, so most of them do something now. A few of the settings still don't do much, but for the most part they work. Play with them and get a combo that works for you. The ones that generally have the biggest impact are the shadow quality (which may also toggle the volumetric fog at the bottom), volumetric fog, and global illumination quality. The rest seem to have little impact most of the time. 
  
* The audio and input settings pages exist, but are not currently hooked up to whatever the default was, so messing with those may cause (more than the expected amount of) wonkiness.

## Gameplay notes:

### Menu things
* ~~The menu is currently absolutely massive. Get over it until I fix it. Should be done in the next release.~~ Fixed it.
* When you die, you need to restart the game. Currently it completely destroys the player entity, so your controls to access the menu are also destroyed. If the camera just starts floating in the sky and you can no longer do anything, you've died. Git Gud. I'll make a proper death that allows you to restart one day.
* There appears to be a bug with the version of the engine I am using where the entire world will jitter if you try to restart the game through the menu or try to switch maps (which is why everything is in one map now). This is not fixable without upgrading the engine version, which will require me to modify several plugins that are not yet supported on those versions. I plan to do it one day, but that will be quite a difficult task, so today is not that day.

### Weapon things
* There is a weapon holster system so you don't have to carry guns around with you all the time. It SHOULD exist just over your left and right shoulders and should start out with a pistol in each. You can't see them, but trust me, they're there. To use the holsters, just grab with empty hands to collect the gun stored inside (fun fact, they're actually stored 1km in the sky). If you were holding a weapon and press the grip button with your hand in the holster hitbox, it will swap the weapons. Storing your current weapon in the holster and putting the holstered weapon into your hand. You cannot holster a weapon that is held in both hands because that is just weird. If you managed to even get the gun into the holster hitbox while holding it with both hands, I would be a little impressed, but you just wasted you time and now you look stupid.
* Ammo counts can be viewed on the back of the hand holding the main grip. Until a mag has been loaded, it will show 0/0. Once the mag has been loaded, it will show X/Y where X is the number of rounds in the current magazine and Y is the total number of rounds of that type that you have.
* Guns of the same class share ammo, so all assault rifles use AR ammo, all pistols use pistol ammo, and so on. 
* Ammo boxes with a sparkle effect and a blue beam coming from space will spawn randomly after every round. If you're low on ammo and cannot afford the random box, or just like your gun, you can hunt these down. 3 spawn at the starting area at the beginning of the game. Moving over the ammo boxes will collect them, and it will replenish some ammo for any gun you are holding as well as the guns in your holsters. The amount of ammo given varies by gun type.
* The shotgun is wonky AF. Deal with it. It needs a completely different reload system from everything else and it was hard enough to make easy reloading work for all the other guns, so I never got around to the shotgun.
* You have a knife. Use at your own risk. It will kill zombies in 1 hit, but must be moving at a minimum speed before it will do any damage, so you have to actually swing it. Odds are the zombies will kill you first. The knife exists roughly in front of your right hip and will return there when it is dropped. It's kinda neat and I spent way too much time on it for it to be so completely useless.

### Random things
* I spent WAY too much time working on the highlighting system that draws a yellow highlight outline around any dropped weapons or attachments as well as the ~~last few~~ zombies each round. For the weapons, it will highlight only parts of the weapon you can see. You will not be able to see dropped weapons through objects. For the zombies, it is exactly the opposite. You can only see the outline of obscured zombies. This is mostly to identify zombies that are stuck somewhere or something so that you can progress the game. It will not help you see zombies that are just sneaky and planning to murder you from behind.
* I redid the zombie spawning system so there is a decent chance they will get stuck or spawn outside the map and die. I will fix those issues later, but for now the highlighting is always on so you can see these stuck zombies. Just run away from where they are and they will despawn and respawn nearby your new location. In particularly hilly areas, the zombies will almost certainly spawn under the map.
* ~~Along that note, I fucked up some of the map geometry around the house with the big fancy driveway near the starting area, so zombies get stuck there quite a bit.~~ Fixed it
* ~~Garage doors are weird. I didn't make them. I take no responsibililty for their behavior.~~ Made them better. I still take no responsibility for their behavior though.
* Your HUD shows your current health in the top left, your money in the bottom left, and the round number in the bottom right.
* Sometimes when you release the second hand grip the magazine drops out of the gun. This is purely graphical and I will fix it eventually. For right now, enjoy your imaginary bullets. Sometimes when you drop your main hand grip on a gun, the magazine drops out of the gun. This is NOT purely graphical and WILL cost you your bullets. The bug giveth, the bug taketh away.
* I added a better sky system that included a day/night cycle. Currently it is set to 1 minute of day and 1 minute of night so you don't have to wait around for the time of day to change to see what it looks like. It also includes a weather system, so who knows what kind of hell you will spawn into when you start the game. Good luck! I have not optimized all of the weather and day/night combinations, so certain unlucky combos may cause particularly bad performance. Just restart the game and you will get a new random weather and time of day. Let me know if something is particularly bad so I can focus on optimizing it.

