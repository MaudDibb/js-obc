# js-obc
minecraft one block command generator...in javascript

This gives you a convenient editor that can create so called 'one command block' creations: you place down one command block, paste in an enormous command script, and let the code do the rest.

Heavliy inspired by the methods used by TheRedEngineer (http://www.theredengineer.com) to easily create these scripts. Note that this only supports Minecraft 1.12.2 command syntax, other versions may be in the works. Do not ask...or fork it and do it yourself ;)

# Installation 
just download index.html and open in your favorite browser. Initially tested with Chrome 65. If it breaks in other browsers, let me know.

# Usage
enter your commands, one line at a time, into the big box in the middle of the screen. Its ok if the lines wrap around, as long as each command is on its own line, and most importantly, *separated by carriage returns*. Do not lump multiple commands into one line. Let the script do that for you. Click on 'One Command!' to generate the command string in the text box on the bottom of the page. Open Minecraft (1.12.2), start a map, give yourself a command block and copy-pasta this command into the command block gui in Minecraft, and activate the block. thats it.

# Notes
this script adds the 'falling-block' passengers trick to make all the commands you enter work. No need to worry about the details, the script will automagically add the proper commands for you. just enter in the commands your creation needs, the script will take care of the rest, including escaping double quotes and slashes where needed. Bless TheRedEngineer for the redstone block/activator rail trick...that is what makes this whole thing possible

# Lag with many repeating command blocks

Some creations may need repeating blocks...some may need MANY repeating command blocks (my lights out game uses almost 50). If you do use them, *please* make sure you add TrackOutput:0b to their datatags...this will eliminate lag as these blocks (in always active mode) run at 20 ticks per second..when you have many of these ticking along at that speed, they will constantly update their previous output field (open one and look at the command gui, that text box showing previous output..ya. thats the one), causing a lot of chunk updates. You might consider doing that to any other blocks chained off those repeating command blocks.
