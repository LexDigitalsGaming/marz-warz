# marz-warz
Text Based MMO Strategy Empire Building PHP Game

Hi
I am new to coding a text based game. And php in general.
But that won't stop me from trying to create this complex game.
My inspiration comes from playing a few awesome text based mmo strategy empire games
called Galaxy Wars, Moonbase, Zorg Empire, cybernations and a few others.

Marz Warz is set in the year 2160 after humans finally destroyed earth and started colonizing Mars.
Few years later people started arguing as to who should be the ultimate ruler on mars.
Like any human argument, it quickly spiraled out of control just as the birth rate skyrocketed.

Players gets to take control of one piece of plot at the start of the game.
They need to construct buildings, produce resources and train armies.
Eventually they get to construct or train a unit called an explorer.
They can move the explorer to an "unclaimed plot" in which ever area or zone
by looking at their radar page.
Once they claim that plot, the explorer disappears and the plot gets added to the users other plots.
Each user can have a total of 15 plots.
Each new plot discovered will work the same,have the same buildings and etc. They player will need to upgrade them all.
Players can attack, raid and defend from attacks from other players which then points will be added to the leaderboard.
Raider points you get when you raid or loot resources from other players.
Attacker points you get if you successfully attack another player and kill their defending armies.
Defender points you get when you successfully defend against an attack.
Each week the leaderboard resets and the top players will get a medal.
Players will also be able to create an alliance with other players. 
Each alliance can hold up to 100 other players.
I will work on alliance feature later in the game.

The buildings each players base or plot will be the following.

Buildings: <br>
Lead mine - max level of 20. Produces 13000 lead per hour at maxed level. <br>
Metal mine - max level of 20. Produces 13000 Metal per hour at maxed level. <br>
Oil well - max level of 20 produces 13000 Oil per hour at maxed level.
Coal mine - maxed level 30 prodeces 70000 Coal per hour at maxed level.
Lead store - maxed level 50. Stores 560 000 lead at maxed level.
Metal store - maxed level 50. Stores 560 000 Metal at maxed level.
Oil silo - maxed level 50. Stores 560 000 Oil at maxed level.
Coal store - maxed level 50. Stores 560 000 Coal at maxed level.
Radar - maxed level 15. Each level gives access to an additional 50 areas.
Research - maxed level 20. Each level allows the user user to research unit movement speed and unit production speed.
Military base - Maxed level 20 upgrade each level will unlock a new military unit.
Anti ICBM - level 10 will act as a defense to defend against player bombing and destroyed buildings. at maxed level it reduces the bomber fighters attack hp by 50%.

Each upgrade they do on each building level. Will add 20 population per level. The population will be added to the players total population.
When a player bombs another players building. For each level that is lost on that building. It looses 20 population and it will show next to the defending players current pop in negative.

There will be a chat feature aswell that sort of acts as a global chat for all players to chat to each other. 

The military units will be trained or built in the military base building page.
The military units and requirements to build them are as follows:

Infantry - MB level 1. 50 of each resources except coal.
Carry capacity of 60 total resource. 
Attack hp - 80
Defense hp - 20
Build time with level 0 research - 1m 45s

Armored buggies - MB level 2. 110 of each resources except coal.
Carry capacity of 100 total resources.
Attack hp - 40
Defense hp - 110
Build time - 2m 30s

Multiple Missile Launchers - MB level 3. 260 of each resources except coal. 
Carry capacity of 90.
Attack - hp - 210
Defense hp - 300
Build time - 4m 10s

Assault Tanks - MB level 6. 1050 of each resource except coal. 
Carry capacity of 130.
Attack hp - 1000
Defense hp - 840
Build time - 15m 10s

Bomber Fighters - MB level 7. 9000 of each resources except coal 
Carry capacity of 0
Attack hp - 100 (the attack hp only affects buildings)
Defense hp - 10
Build time - 35m 0s

Plasma Fighters - MB level 7. 5800 of each resources except coal. 
Carry capacity of 0
Attack hp - 1600
Defense hp - 1300
Build time - 31min 0s

Transport Trucks - MB level 8. 720 of each resources except coal. 
Carry capacity of 1020.
Attack hp - 10
Defense hp - 15
Build time - 11m 10s

Transport Choppers - MB level 9. 910 of each resources except coal. 
Carry capacity of 2100.
Attack hp - 20
Defense hp - 25
Build time - 12m

Air Frigates - MB level 15. 6300 of each resources including coal.
Carry capacity of 2500.
Attack hp - 1300
Defense hp - 990
Build time - 21m 20s

Air Cruisers - MB level 16. 8500 of each resources including coal.
Carry capacity of 3800.
Attack hp - 1600
Defense hp - 2300
Build time - 26m 50s

Air Battleships - MB level 18. 13000 of each resources including coal 
Carry capacity of 1200.
Attack hp - 4000
Defense hp -2800
Build time - 32m 16s

Explorer Crew - MB level 20 (max) 60000 of each resources including coal
Carry capacity of 0
Attack hp - 0
Defense hp - 0
Build time - 1h 40m 0s

Next to each military unit type or name. There will be in brackets display the amount of units they have for each unit and next to it in green +how many units are training.
You can train or build more than one type of unit at a time. It will look like the following:
Infantry: (2000)+3000
That means the player has 2000 infantry and 3000 are busy being built.
Then on the main overview page (index.php) next to the (Military Base) link or button. In brackets and pink. It will show the overall total number or troops.
Example. 
Military Base (230000)
Player has 230000 units in total on that base

Now for the radar section

Radar
The way Im going to display the radar and "unclaimed plots" to the players will be the following:
PS. I give a lot of credit to the admin of Galaxy Wars for this radar.

Players base will essentially be coordinates to their base other players can use to attack, defend or even send resources to.
The format of the coords will work like this:
The Radar will consist of 100+ Areas, 30 Zones for each Area and 15 Plots for each Zone.
When registering an account a player will be assigned a random base coords for their first base.
It will display next to their name in this format. 
PlayerName - (A50Z5P11)
Meaning this players one base can be found in Area 50, Zone 5, Plot 11.
When other players see this on their radar, it will be in this format:
A50Z5P11 - PlayerName.
Clicking on the players coords will take the other player to the bases overview page which only show the Popultion of that base, the day it was created and the player who ownes it.
Additionally below the above info, there will be buttons for the following:
Attack
Move.
You can also click the players name at the very top of the base page which will bring up the player who owns that base details which will only show the following:
PlayerName - Total population (which is all bases popultion combined)
Alliance name (which you can click on to view the alliance it self (later stages)
Raider Points
Attacker Points
Defender Points
Attacker Medal
Defender Medal
Raider Medal.
Then a button
Send Message.

The way the database must display all the players bases will be that it will READ all players base coords and display it onto the radar page.
There will be a form to search the areas and zones as well as next and previous buttons to navigate the radar.
At radar level 0 you can only view the first 5 pages of the radar from your current base, left to right.
Upgrading the radar unlocks extra 5 pages per level.
(I hope I get to make it work).

Now back to the military section but first I want to explain how the each players overview page will look for each and every base they own.

Once a player succefully registers their account, they must be redirected to their individual overview page and it will look like this.
=========
PlayerName - (A50Z5P11) (Once players claim more and more plots, it will display next to all their other plots. Clicking on the plot will take you to that bases overview page which will display the exact same stuff except for pop and resources and troop count. The upgrades will also differ as player needs to upgrade the same buildings on all bases individually)
Pop (10000)
L:5000 - M:5000 - O:5000 - C:5000

Alerts: (Will be used to display all army activities)

Progress: (Will be used to display all building activities and army productions with times)
Lead mine to lvl (5): 6m 3s
Infantry: 2m 5s (+45000)
Reasearch to lvl (6): 4m 5s

Construction Menu:
Buildings (will be a button to the build.php page that has all the buildings you can upgrade)
Research (same as buildings but just for research.php)

Military Menu:
Radar (radar button that takes you the radar page and to your current seleced base coords)
Military Base (360000) (a button to all the military units where you can construct or train them. Only Military Base will be a button not the troop count)
Mailbox (1) (will be a button to your mail box, the number 1 next to indicates this player has one unread mail)
Forces (50) ( a button where you create groups called battalions where you then insert your army in or which ever unit you require or need, 50 indicates this player has 50 battalions created)

Chat | Help| Leaderboard| Logout (the footer of the page with links that does what they are called.
==========

Now I will show you what each page will have to look like starting from the construction section:

Buildings: (After the player clicks on the buildings button)
=
At the very top of the buildings page it will display that players name, select base coords and available resources available for that base and then that base pop.
Then it will display the following:

Coal Mine Lvl (5)
Cost: L:100 - M:100 - O:100 - C:100 - (+20) (those are the resources required for next upgrade and the +20 is the pop it that will be added to the bases total pop)
Time: 5m 6s (that is the time it will take before its upgraded to level 6)
Health:500 hp (That is the amount of bomber fighters attack hp required to reduce it 0 healt which destroys it once at 0 health. PS. Just an example)

Lead Mine Lvl (5)
Cost: L:100 - M:100 - O:100 - C:100 - (+20) (those are the resources required for next upgrade and the +20 is the pop it that will be added to the bases total pop)
Time: 5m 6s (that is the time it will take before its upgraded to level 6)
Health:500 hp (That is the amount of bomber fighters attack hp required to reduce it 0 healt which destroys it once at 0 health. PS. Just an example)

Metal Mine Lvl (5)
Cost: L:100 - M:100 - O:100 - C:100 - (+20) (those are the resources required for next upgrade and the +20 is the pop it that will be added to the bases total pop)
Time: 5m 6s (that is the time it will take before its upgraded to level 6)
Health:500 hp (That is the amount of bomber fighters attack hp required to reduce it 0 healt which destroys it once at 0 health. PS. Just an example)

Oil Well Lvl (5)
Cost: L:100 - M:100 - O:100 - C:100 - (+20) (those are the resources required for next upgrade and the +20 is the pop it that will be added to the bases total pop)
Time: 5m 6s (that is the time it will take before its upgraded to level 6)
Health:500 hp (That is the amount of bomber fighters attack hp required to reduce it 0 healt which destroys it once at 0 health. PS. Just an example)

Coal Store Lvl (5)
Cost: L:100 - M:100 - O:100 - C:100 - (+20) (those are the resources required for next upgrade and the +20 is the pop it that will be added to the bases total pop)
+13000 KGs (that is the amount of storage added after the upgrade)
Time: 5m 6s (that is the time it will take before its upgraded to level 6)
Health:500 hp (That is the amount of bomber fighters attack hp required to reduce it 0 healt which destroys it once at 0 health. PS. Just an example)

Lead Store Lvl (5)
Cost: L:100 - M:100 - O:100 - C:100 - (+20) (those are the resources required for next upgrade and the +20 is the pop it that will be added to the bases total pop)
+13000 KGs (that is the amount of storage added after the upgrade)
Time: 5m 6s (that is the time it will take before its upgraded to level 6)
Health:500 hp (That is the amount of bomber fighters attack hp required to reduce it 0 healt which destroys it once at 0 health. PS. Just an example)

Metal Store Lvl (5)
Cost: L:100 - M:100 - O:100 - C:100 - (+20) (those are the resources required for next upgrade and the +20 is the pop it that will be added to the bases total pop)
+13000 KGs (that is the amount of storage added after the upgrade)
Time: 5m 6s (that is the time it will take before its upgraded to level 6)
Health:500 hp (That is the amount of bomber fighters attack hp required to reduce it 0 healt which destroys it once at 0 health. PS. Just an example)

Oil Silo Lvl (5)
Cost: L:100 - M:100 - O:100 - C:100 - (+20) (those are the resources required for next upgrade and the +20 is the pop it that will be added to the bases total pop)
+13000 KGs (that is the amount of storage added after the upgrade)
Time: 5m 6s (that is the time it will take before its upgraded to level 6)
Health:500 hp (That is the amount of bomber fighters attack hp required to reduce it 0 healt which destroys it once at 0 health. PS. Just an example)

Radar Lvl (5)
Cost: L:100 - M:100 - O:100 - C:100 - (+20) (those are the resources required for next upgrade and the +20 is the pop it that will be added to the bases total pop)
+5 (that is the amount of new radar pages that will be unlocked)
Time: 5m 6s (that is the time it will take before its upgraded to level 6)
Health:500 hp (That is the amount of bomber fighters attack hp required to reduce it 0 healt which destroys it once at 0 health. PS. Just an example)

Military Base Lvl (5)
Cost: L:100 - M:100 - O:100 - C:100 - (+20) (those are the resources required for next upgrade and the +20 is the pop it that will be added to the bases total pop)
Time: 5m 6s (that is the time it will take before its upgraded to level 6)
Health:500 hp (That is the amount of bomber fighters attack hp required to reduce it 0 healt which destroys it once at 0 health. PS. Just an example)

Anti ICBM Lvl (5)
Cost: L:100 - M:100 - O:100 - C:100 - (+20) (those are the resources required for next upgrade and the +20 is the pop it that will be added to the bases total pop)
Time: 5m 6s (that is the time it will take before its upgraded to level 6)
Health:500 hp (That is the amount of bomber fighters attack hp required to reduce it 0 healt which destroys it once at 0 health. PS. Just an example)

Home | Help |
===============
