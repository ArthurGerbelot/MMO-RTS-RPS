# Project code MMO-RTS-RPS

## Summary


## The Universe

 - The universe contain multiple **galaxies** *[0-max]*
 - Each **galaxy** contain multiple **spiral arms** *[0-4,6,8?]* with **solar systems** *[0-99999+]* (`0` is the closest to the center)
 - Each **solar systems** contain **planets** *[0-max]* (`0` is the closest to the sun(s))
 - **Planets** can have moons 
 

The planet position is defined by `galaxy-spiralArm-solarSystem-planet`. Can be considered as an unique Id.*(Example: 2-3-150354-3)*
