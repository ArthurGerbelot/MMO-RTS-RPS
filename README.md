# Project code MMO-RTS-RPS

## Summary


## The Universe

#### Hierarchy
 
 - The universe contain multiple **galaxies** *[0-max]*
 - Each **galaxy** contain multiple **spiral arms** *~[0-4,8] with **solar systems** *[0-99999+]* (`0` is the closest to the center)
 - Each **solar systems** contain **planets** *[0-max]* (`0` is the closest to the sun(s))
 - **Planets** can have moons 
 - **Planets** have **cities** and **outpost** (see *City/Outpost*)
 
The planet position is defined by `galaxy-spiralArm-solarSystem-planet`. Can be considered as an unique Id. *(Example: 2-3-150354-3)*

#### Facts

 - New player are populated the border of the galaxy (far for the center, where the **solar system** number is high)
 - More the player are close to the center, more the game is difficule (see *IA/Pirates*) but interesting in resources

## Planets - Cities/Outposts

#### Planets

 - **Planets** have a random:
   - size defined by the number of **regions** *~[1-5]*
   - temperature, color, ..
 - **Regions** have an unique **city** and a random number of **outpost** *~[2-6]*
 
#### Cities/Outposts

 - The **city** is the main part of a region. The player who control that city, gain the region's resources
 - If the owner of **city** also have **outpost** (on the same region), he will receive bonus (Ex: +10% resources, can have a special building, ..) 
 - Every player can take an **outpost** by attacking it (maybe not the first time)
 - **City** can NOT be taken if a player already have it. Only owner can decide to leave a city. (see *Colonization*)
 - **City** have a maximum of building, defence and unit that can contain (see *Buildings-QG*)

## Players

 - **Player** start on a new planet with only 2 unpopulated cities.
 
## Space Exploration / Colonization

 - **Solar system** view are available with **Radar** lvl 1 (see *Buildings*)
 - **Galaxy** view are available with **Radar** lvl 2 (see *Buildings*)
 - The range of Galaxy view is defined by Radar lvl and Technologies 

## Quests
 
#### Tutorial
 
 - Quests help user to start as tutorial:
   - Build **Generator** 
   - Build **Mine** 
   - Build **Troop camp**
   - Attack an **Outpost** on your city's region (can't take it now)
   - Build **Vehicule Factory**
   - Build **Outpost Vehicule deployment** and take control of an **Outpost** on your city's region
   - Build **QG Vehicule deployment** and take control of an **City** on your planet
   - Build **Space Radar**

#### Event

 - Random even can append as quest. (see *IA/Pirates*)

## Raid (Tower defense)

 - Player can attack another player (or an IA) even if the target isn't logged
 - The player who want to attack have to move **Troops** using **Transport Ship** (See *Units** and **Fleet**)
 - A tower defense start between:
   - Defence with the **city/outpost** as base
   - Attack with **troop** and **special power** available on the **fleet**

## IA/Pirates

 - No-player **cities/outposts** are auto-generated by the game on random planet
 - **Players** can attack their base (who can be destructed)
 - Random even can append (cities/outposts attack, ship interception, ..)
 - More close planet are from the center of the galaxy, more evolued are the IA, more interesting are resources

## Multiplayer games 
 - Coming later (much later)

## Alliance / Relation

## Buildings

#### QG (city only)
<img src="http://preview.turbosquid.com/Preview/2014/07/09__08_24_48/view0.pngbaa4c4a6-aef3-4c25-a9e2-d9c788b77845Original.jpg" width="150px" />

 - Main building, auto-created when a player take control of a city (require **QC Vehicule deployment**)
 - The level of this building limit the maximum number of buildings that city can contain 

#### OutPost (outpost only)
<img src="http://preview.turbosquid.com/Preview/2014/07/10__00_40_15/V1.png72e149e2-51ef-4aaf-99b4-5266d13a3c8fOriginal.jpg" width="150px" />
 
 - Equivalent as **QG** for an outpost  (require **Outpost Vehicule deployment**)

#### Generator (city only)
<img src="http://preview.turbosquid.com/Preview/2014/07/09__20_21_44/v6.png2fcbb516-4406-4af9-a3d4-c4c1efd54a85Original.jpg" width="150px" />

 - Create energy
 
#### Solar panel

 - Create energy
 
#### Mine (city only)
<img src="http://preview.turbosquid.com/Preview/2014/07/09__10_09_01/Reactor_v1.png001d08eb-7238-4aa9-a7b1-04f2c0845774Original.jpg" width="150px" />

 - Collect resource

#### Silo (city only?)
<img src="http://preview.turbosquid.com/Preview/2014/07/09__21_25_32/v1.png25cd7859-9e0c-4b2e-9371-e38b3fdf55ccOriginal.jpg" width="150px" />

 - Store more resources
 - **Requirements:**
   - Mine lvl 4   

#### Space radar (city only)
<img src="http://preview.turbosquid.com/Preview/2014/07/09__21_46_14/v1.png6a7996e9-c2e6-4098-a9fe-2f5df5a62514Original.jpg" width="150px" />

 - Used for space exploration
 - Allow user to detect interesting planet
 - **Requirements:**
   - QG lvl 3  

#### Troop Camp (city only)
<img src="http://preview.turbosquid.com/Preview/2014/07/09__21_25_32/V1.pngcb8c46f8-0b2d-49a2-b3fb-83ea7caab9b4Original.jpg" width="150px" />

 - Create troops

#### Vehicule Factory (city only)
<img src="http://preview.turbosquid.com/Preview/2014/07/09__22_36_02/V1.png743e5ecf-0ac4-4692-ab8b-3bfd1cd120d0Original.jpg" width="150px" />

 - Create vehicules

#### Laboratory (city only)
<img src="http://preview.turbosquid.com/Preview/2014/07/09__10_23_50/v1.png3dc291cf-7970-498f-9c6c-dc8017078203Original.jpg" width="150px" />

 - Make some research to unlock technologies

#### Space docker (city only)
<img src="http://preview.turbosquid.com/Preview/2014/07/09__10_44_42/V1.pngbcbb2100-3f8e-4dac-ae4f-a94fe028bf87Original.jpg" width="150px" />

 - Allow user to stationnate ship on a city (see *Fleet*)
 - Control your fleet, send space traval or attack from here

#### Turret
<img src="http://preview.turbosquid.com/Preview/2014/07/09__09_45_57/V1.png68a86448-ae3f-4f87-b6b9-e86f2f399183Original.jpg" width="150px" />

 - Defence

## Reseach

## Troops

#### Troops

#### Vehicules

**Outpost Vehicule deployment**
 - Allow to take an outpost when attacking, and create Outpost building.
 - **Requirements:**
   - Vehicule Factory lvl 1
   
**QG Vehicule deployment**: 
 - Allow to take a city when not occupied (or IA attacking), and create QG building.
 - **Requirements:**
   - Vehicule Factory lvl 2

## Fleet

#### Troops Transport Ship

 - Allow use to transport troops from planet to another, or attack
 - 
#### Resources Transport Ship

 - Allow use to transport resources from attacking planet, or from a planet/city to another.

#### Canon Support Ship

 - Instead of transporting troop, this ship add a `special power` for the player during Tower Defence or Mutiplayer games (see *Special powers*)


## Special powers

 - Instead of transporting troop, some ship add a `special power` for the player during Tower Defence or Mutiplayer games (See *Fleet*)

