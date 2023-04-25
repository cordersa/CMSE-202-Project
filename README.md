# CMSE-202-Project: Rock Climbing
Ibrahim Elsadek, Sam Barans, William Voigt, Samuel Corder

## IMPORTANT NOTE: We had issues with sharing the project on Github, so there are several versions of the file from each contribution. **The most up to date version as of right now is the 4/23 file!**


This code is designed for simulating a rock climber climbing a wall. The user may input several statistics about both the climber and the wall before running the simulation. The simulation will display the climber climbing the wall, and it will stop when the climber falls

Besides simulation, there are also several functions used to calculate statistics so we can compare different climbers. These are specific to our CMSE 202 Project, but can be used as a template as well.


### Class: Climber - This is the climber that will climb our wall.

Attributes:

    reach - radius of movement for the climber
    sloper - climber strength on slopers
    crimp - climber strength on crimps
    jug - climber strength on jugs
    heights - list of heights reached by the climber on a series of walls
    icon - marker for visuals the climber is in
    position - coordinates for the climber on a wall
    
Methods:

    make_move() - evaluate if it is feasible to 'stick' a move to one of the holds on the wall or if the climber falls and does not reach any with their given abilities
    average_h() - returns the average height the climber achieved on the walls it was run on
    set_position() - Sets position, can be used to reset after climbing a wall



### Class: Hold - Holds are the term used for the rocks on a rock wall. There are several different kinds, which is why we are creating a separate class.
Attributes:

    coords - coordinates of the hold 
    type - sloper, crimp, or jug


### Class: Cell - This is one chunk of our wall. We created a “Cell” and a “Wall” class so that we could make the wall whatever size we wanted without the holds being too spread out by poor RNG.
Attributes:

    slopers - number of sloper holds
    crimps - number of crimp holds
    jugs - number of jug holds
    height - height of the cell along the wall should be multiple of 10
    holds - array of hold objects in the cell
    hold_types - list of types of holds
    
Methods:

    show() - plots cell


### Class: Wall - This class is where everything comes together. This class compiles the cells and runs the climber on the wall.

Attributes:

    slopers - number of sloper holds
    crimps - number of crimp holds
    jugs - number of jug holds
    height - height of the cell along the wall. should be multiple of 10
    holds - array of hold objects in the cell
    x - array of x coordinates of the holds
    y - array of y coordinates of the holds
    hold_cords - list of coordinates of the holds
    total_holds - number of total holds
    hold_types - list of types of holds
        
Methods:

    show() - plots wall
    run_wall() - takes in a climber object and simulates the climber attempting to climb the wall. Returns a list of all points the holder occupied during their path
    plot_path() - stores a GIF of a climber moving up the wall, drawing a line to each hold for the moves made


**Everything Below the Classes is specific to our CMSE 202 Project.**
To summarize what we did specifically, we created 400 climbers, 100 of each in categories, being all around, good at slopers, good at crimps, and good at jugs. We then ran these on 20 randomized walls to see which group performed the best, in order to answer the question: **What Type of Skillset is Optimal for Rock Climbing?** We also created a linear regression model for this code.

```python

```
