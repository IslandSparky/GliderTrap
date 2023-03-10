#GliderTrap
This application is used in conjunction with GliderView to look for Game of Life "gliders" (also called
"spaceships") which are patterns in the Game of Life that move across the "world" in a way that preserves
their form. This application is part of a pair used to search for larger gliders (those above 5 active cells).

This program provides for quickly running through many interations of the Game of Life using random
starting configurations in order to find those runs that might contain interesting large gliders.  In order to do this, the program  writes records saving the random starting configurations for runs of the game that produce outcomes that reach the edge of the game "world". A large percentage of the records in this file (about 9 out of 10) do not represent interesting glider finds.  Instead, they represent cases where the game has simply grown to reach the game boundaries. True large gliders are evident by the fact that they reach the world boundary well ahead of the normal spread of the patterns in the world.

By using the companion program GliderView on this preview.dat file, the user quickly review the records in preview.dat to see if they produce big gliders of interest.  

## Usage 

The program will open the world view and begin executing. Each interation begins automatically and will stop when the boundaries of the world are reached or the game reaches a steady state of population and area. If the world boundaries are reached, a record will be written to the file "preview.dat" for later 
review using the program GliderView. If the boundaries are not reached, execution will automatically begin with the next random starting configuration. 

It is quit common that the game will generate small gliders containing five active cells. These are considered to be of no interest and are deleted when they reach the world boundary with no effect on execution and no record being written.
 
During execution, assuming focus is on the world display, the following keys are available to control the execution of the Game of Life.

'esc' will exit the program

'left arrow' pauses execution.

'right arrow' resumes execution.

'up arrow' speeds up execution. It may be held down to rapidly increase game speed.

'down arrow' slows execution in order to examine details. It may be held down to rapidly decrease game speed.

'd' key toggles the display mode.  When display is turned off, the game will very rapidly execute until
        the final state when the world boundary is reached. In this way many interations of the program may be done quickly. 

'r' key replays the current world   so that execution may be re-examined. 

'space' move the game to the next random starting configuration. 

