# README

* ⚠️ **WIP**  
* ✅ **GREEN**  
* 🧠 **In Discovery**  
* ❌ **RED**  
* 📝 **TBD**  

US
As a pirate ship captain I want to be able to tell if a given course on a map is safe from Royal Navy patrols

The map marks the locations of the pirate ship and Royal Navy ships.

The pirate ship moves west to east and is safe when it reaches the edge of the given map

The Royal Navy ships starts on the top and bottom rows of the map and move north to south, 
switching direction when they reach the edge of the map

All ships move at the same speed, and moves one square per time unit

The pirate ship is caught if any Royal Navy ship is within one square of it at any time

UAT
Given a map of the ships positions, return true if the pirate ship can reach the edge of the map without being caught
by the Royal Navy ships, otherwise return false

The map is a given as a 2d-grid with the positions of the pirate ship (marked as X), 
the Royal Navy ships (marked as N), and empty ocean tiles (marked as 0).

The pirate ship moves from west (left) to the east (right)
The pirate ship is safe when it reaches the edge of the map
It moves one square per time unit

The Royal Navy ships start on the top and bottom rows of the map
If it starts on the top row, it moves south
If it starts on the bottom row, it moves north
When it reaches the edge of the map, it switches direction
And always moves one square per time unit