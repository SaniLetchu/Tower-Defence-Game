# Meeting Notes
In this file, you are required to take notes for your weekly meetings. 
In each meeting, you are required to discuss:

1. What each member has done during the week?
2. Are there challenges or problems? Discuss the possible solutions
3. Plan for the next week for everyone
4. Deviations and changes to the project plan, if any

***

# Meeting 09.11.2021 12::00

**Participants**: 
1. Daniel Nikkari 653088
2. Sani Letchu 715036
3. Oskari Kiili 728890
4. Vili Nieminen 593465


## Summary of works
Everyone configured their development environment and installed SFML and tested compiling a simple program with it.

1. Daniel (20h)
   
   Built the game foundation: main calls game and game interacts with different objects to run the game. See `src/` for details.
   Implemented state base class and state stack system so the game state calls different states and pops them after to return to previous state.
   Implemented main and menu states, and entity base class. Created a button class.
   Included `src/Config` for `.ini` files to separate configuration from code. 

2. Sani (8h)

   Built initial highscore state and map builder.  

3. Oskari (6h)

   Tested different implementations and set up Windows Subsystem for Linux further. 


4. Vili (7h)

   Devised and documented a Git branching workflow (simplified Gitflow with only develop). 
   Compared and chose testing framework (Catch2).  


## Challenges

1. Getting the map builder working: after it runs game dynamics can be tested easier. 
   An open question is to how to define the road where enemies move, textures for it are ready and there are a few ideas for implementation.
2. Choosing the coordinate system, screen pixels vs. game tiles, to compare distances


## Actions
1. Get the map working
2. Have a working Makefile for easier compilation and testing
3. Code other parts with no direct dependencies to map


## Project status 
We are ahead of schedule and Daniel has built a good base for building the game on. Everyone is starting to get a working development environment and as the next steps are clearer it is easier to allocate work. 


### TODOs
1. Daniel: Rest.
2. Sani: Try to finish map builder for next week.
3. Oskari: Implement enemy classes
4. Vili: Read up on the code base and build an initial Makefile


***

# Meeting 21.11.2021 13::00

**Participants**: 
1. Daniel Nikkari 653088
2. Sani Letchu 715036
3. Oskari Kiili 728890
4. Vili Nieminen 593465


## Summary of works

1. Daniel (6h)
   
   Improved menu with buttons and animation

2. Sani (5h)

   Got map builder working such that only one path is acknowledged with one starting and end point.  

3. Oskari (3h)

   Worked on Entity class to a point where it requires still movement functionality

4. Vili (11h)

   Created a Makefile for building the project. 
   Setup Doxygen and created an example template for documenting classes (`button.hpp`)


## Challenges

1. NPC interaction on the map; choosing the coordinate system, screen pixels vs. game tiles, to compare distances?


## Actions

1. Finish entity class with movement functionality on the map (Oskari)
2. Save multiple maps with different names (Sani)
3. Finish Doxygen documentation for all relevant classes


## Project status 
We are still in schedule but unfortunately many people have had other tasks that have taken a lot of time from this project. If we can get working NPCs on the map next week we are nearing a working game in time.


### TODOs
1. Daniel: Tower placement on the map
2. Sani: Save multiple maps with different names
3. Oskari: Finish entity class with movement functionality on the map 
4. Vili: A little busy up to midweek, take the most relevant task at hand then


***

# Meeting 28.11.2021 13::00

**Participants**: 
1. Daniel Nikkari 653088
2. Sani Letchu 715036
3. Oskari Kiili 728890
4. Vili Nieminen 593465


## Summary of works

1. Daniel (1h)
   
   Did thesis

2. Sani (+30h)

   Created a textbox class for button
   Map selector state and named map savings to a file
   Little bit of NPC and gaming state classes

3. Oskari (+20h)

   NPC class movement (rotation, speed etc.) and damages
   Some memory management

4. Vili (0h)

   Did other courses


## Challenges

1. If we want to spawn multiple guys from one NPC, it is difficult to spawn them randomly to other nearby pixels due to current movement logic


## Actions

1. Different subclasses for NPC
2. Logic for building a round: how many NPCs and of different classes
3. Animation for shooting
4. Audio for NPC and towers


## Project status 
We are a little ahead of schedule as Sani and Oskari did a lot of valuable work for getting the NPCs and maps working with only little crashing and little to none memory leaks. Daniel is about to finish his thesis so he can also put in hours, but Vili is still tied with other stuff and tries to get everything out of the way so he can contribute more in the final week. The aim is to get a minimum working game at the end of next week so we have some time to debug details and polish the game with extra features.


### TODOs
1. Daniel: Audio and general work
2. Sani: Map building logic
3. Oskari: NPC extensions
4. Vili: Try to finish other courses


***

# Meeting 4.12.2021 13::00

**Participants**: 
1. Daniel Nikkari 653088
2. Sani Letchu 715036
3. Oskari Kiili 728890
4. Vili Nieminen 593465


## Summary of works

1. Daniel (3h)
   
   Improved scrolling functionality in the user interface

2. Sani (+30h)

   UI for resources, money system etc.
   Tower placing on map
   Round system for enemy waves

3. Oskari (4h)

   Enemy NPC subclasses

4. Vili (0h)

   Did other courses


## Challenges

1. If we want to spawn multiple guys from one NPC, it is difficult to spawn them randomly to other nearby pixels due to current movement logic
2. We currently have game parameters hardcoded in the source code; these should be separated into a file so tweaking the game is easier and the code easier to read
3. There is still some random, inconsistent crashing when enemies reach the end of the map. We are unsure whether this has to do with the movement function or destructors (or both)

## Actions

Must do
1. End game when HP = 0
2. Slowing tower logic to mirror bomb tower
3. Tank spawns multiple basic NPCs
4. Few more maps with different level of difficulty in layout
5. "Enemies left" counter on the map UI
6. Parameters into separate file
7. Scroll off from map selector
8. Fix memory leaks and warnings
9. Create PDF documentation from Doxygen instead of HTML
10. Create project documentation, see [instructions](https://plus.cs.aalto.fi/elec-a7151/2021/M6-Projects/guidelines/#project-documentation)

Extra (additional features):
1. Sound effects for towers
2. Separate high scores for different maps


## Project status 
We now have almost a working game; the only thing left for minimum requirements is that the game should end when the hitpoints reach 0, tank spawn more NPCs and a few maps. Outside the game, we should improve our documentation a little and at the end produce the required project documentation. With leftover time, we try to balance the game such that the actual playing experience is enjoyable. 



### TODOs
Everyone has to check on action 8. of memory leaks and warnings, we'll see the work distribution for 10. project documentation closer to the deadline
1. Daniel: Extra 1, 2
2. Sani: 1, 2, 5, 7
3. Oskari: 3, 4
4. Vili: 6, 9


***
