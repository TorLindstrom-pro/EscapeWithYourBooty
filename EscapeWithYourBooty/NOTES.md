# Notes

* ⚠️ **WIP**  
* ✅ **GREEN**  
* 🧠 **In Discovery**  
* ❌ **RED**  
* 📝 **TBD**  

### Goal: 
### Time 🍅
### Notes:

#### Pseudocode

* Create ships from map
* Loop until safe
  * Move ships
  * Check if caught -> return false
* Safe -> Return true

#### Domain Objects/ UATs

Pirate ship:
* has a given row
* has a current column
* can move, increasing the column by 1

Royal Navy ship:
* has a given column
* has a current row
* has a start direction
* can move in its current direction changing the row by +/-1
* switches direction when it reaches the edge of the map
  * knows if it has reached the edge of the map

CourseChecker:
* takes a map as a 2D array of characters
* returns true if the passage is safe
* returns false if the pirate ship will get caught

#### Tests

1. Create domain objects
   1. Pirate ship
      1. has a given row
      2. has a current column
      3. can move, increasing the column by 1
   2. Royal Navy ship
      1. has a given column
      2. has a current row
      3. has a start direction
         * start row == 0 -> direction = south
         * start row != 0 -> direction = north
      4. can move in its current direction changing the row by +/-1
      5. switches direction when it reaches the edge of the map
         * IN edge: 3, row: 2, direction: south -> OUT row = 3, direction = north
2. CheckCourse
   1. [[0, 0, 0, 0]] -> true
      * ℹ️ creates the method, sets the parameters, and return type
   2. [[X, 0, 0, 0]] -> true
      * ℹ️ creates the pirate ship object here, and move it until it's safe
   3. [[X, 0, 0, N], 
       [0, 0, 0, 0],
       [0, 0, 0, 0],
       [0, 0, 0, 0]] -> true
      * ℹ️ creates and moves Royal Navy ships
   4. [[X, 0, 0, 0], 
       [0, N, 0, 0]] -> false
      * ℹ️ creates logic to check if caught 
      * (can maybe be a theory)
   5. [[X, 0, 0, 0, N], 
       [0, 0, 0, 0, 0],
       [0, 0, 0, 0, 0]] -> false
      * ℹ️ navy ship catches pirate ship efter switching direction, solution is finished