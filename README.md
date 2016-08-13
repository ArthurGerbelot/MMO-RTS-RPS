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


## Players

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

## Buildings/Research

#### QG (city only)
<img src="http://preview.turbosquid.com/Preview/2014/07/09__08_24_48/view0.pngbaa4c4a6-aef3-4c25-a9e2-d9c788b77845Original.jpg" width="150px" />

 - Main building, auto-created when a player take control of a city 

#### Mine (city only)
<img src="http://preview.turbosquid.com/Preview/2014/07/09__10_09_01/Reactor_v1.png001d08eb-7238-4aa9-a7b1-04f2c0845774Original.jpg" width="150px" />

 - Collect resource

#### Silo
<img src="http://preview.turbosquid.com/Preview/2014/07/09__21_25_32/v1.png25cd7859-9e0c-4b2e-9371-e38b3fdf55ccOriginal.jpg" width="150px" />

 - Store more resources
 - **Require:**
   - Mine lvl 4   


#### Space radar (city only)
<img src="http://preview.turbosquid.com/Preview/2014/07/09__21_46_14/v1.png6a7996e9-c2e6-4098-a9fe-2f5df5a62514Original.jpg" width="150px" />

 - Used for space exploration
 - Allow user to detect interesting planet
 - **Requirements:**


## Troops/Fleet


## Space Exploration


## Colonization


## Raid (Tower defense)


## IA/Pirates


## Multiplayer games 


