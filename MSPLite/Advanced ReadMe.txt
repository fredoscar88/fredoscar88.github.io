**This is the advanced readme for users of MSPLite**
**If you haven't read the other ReadMe file, it's 
probably a good idea to do that**

Note: 	It is reccommended that you use a file editor
		(like notepad++), if on windows. If you're a
		linux user, chances are you already have a
		vim or emacs editor that you like to use, and
		the mac default file editor most likely formats
		files in the intended way. It's much harder to
		edit these files if the formatting is off!

Note:	Files are interpreted alphabetically
		Eventually a file named "main.txt" will be
		interpreted before all others as a convenience
		option.

Syntax and keyword guide-
	Certain keywords present in the lines of a
	redstone text file will do different things.
	
SYNTAX	  	| 	FUNCTION
				(written at start of line)
INIT			This line is not placed in a
				command block, but instead executed directly
				from the server when MakeRedstone is called.

				(should be the only thing in the line)
:NEW SET		Starts a new chain of command blocks. If POS
				and PAT are not specified they will default to
				the POS and PAT settings in the MSP.properties file
			
				(written at start of line)
POS <X Y Z>		After ":NEW SET" is written, the position of
				first block can be declared with "POS <X Y Z>",
				with X Y Z being the coordinates of that block
				
				(written at start of line)
PAT <X Y Z>		After ":NEW SET" is written, the pattern that the
				new set will follow in placing blocks is determined
				by "PAT <X Y Z>". Each of those must be at least 1.
				The system will start by adding blocks in the positive
				X direction, and once it reaches that limit will place 
				blocks in the positive Z direction. Once that 
				limit is reached blocks are placed in the positive 
				Y direction. Currently the Y limit is ignored.
				
				NOTE WELL! POS and PAT are not specified after
				":NEW SET" is written then the new set of blocks will
				inherit these properties from the previous set, 
				or the default, meaning that the new set could overwrite
				the old one. Take care when defining sets.
				
				(written at start of line)
CONDITIONAL		Causes that chain command block to become conditional.
				Fair warning, if you aren't careful about what (pattern)
				you are using then these blocks will not end up with a
				command block directly behind them (which is required
				for them to function), so if the redstone is not working
				be sure to check your command chain to make sure there is
				in fact the right command block behind this.

*<string>		Defines a reference point. Reference points are
				chains of command blocks that are not on the
				clock and designed to be activated by impulse
				command blocks. All lines after this syntax are
				placed in that chain.

				(written inside of a command)
-> <string>		Activates the reference point of name <string>.
				In the final version of the command, "-> <string>"
				is replaced by a redstone setblock command.
				
DELAY X			Only to be written in a line after "*<string>".
				Causes a delay between two commands in a reference
				point chain.
----------------------------------------------------------------------

MSP.properties
You can change the default starting position and pattern of new
sets from the file MSP.properties.

You can change the redstone directory. If MSPLite cannot find
the directory, it will create one using the name from MSP.properties.

You can change the script storage directory. If MSPLite cannot find
the directory, it will create one using the name from MSP.properties.

Launch configuration can also be changed to include different option
flags and change the amount of ram used by the server.

If OIT (Output Interpreting) is set to true then you can set up
some players to be able to run certain MSPLite commands from ingame.
	
	In order to set this up, set OIT to true (in MSP.properties) and 
	run MSPLite. This will create a directory called "MSPPlayers"
	
	To give a certain player permissions, create a textfile in the
	MSPPlayers directory following this format: "<playername>.txt".
	Once again it helps if you have file extensions visible.
	
	Inside that a player's text file, simply type "rank=x"
	where x is their rank.
	
	You can open up "cc.text" to view the different commands, wether
	they're enabled, and the minimum rank required to use them.
	
	Sample command format:
	<command>-Enabled=true
	<command>-Rank=1000
	<command>-Cmd=say hi
	
		Whenever a player of minimum rank 1000 types in "<command>"
		the server will run "say hi".
	
	You can add your own commands and change how you call pre-existing
	ones

The script directory contains text files. You can enter in a collection
of commands, call the script in game or from the MSP console, and the
server will run the commands in order.
	
	For example, if inside the script directory there is a text file
	labelled "hello.txt", containing lines "say Hello World!" and 
	"say Good bye, World!" then typing "!Script hello" in game
	(provided the !Script command is enabled and the player has
	the minimum rank) then the server will execute "say Hello World!"
	and "say Good bye, World!"
	
CONSOLE COMMANDS
Console commands can be listed by entering in "help" to the MSP console.
The only command currently not listed, but still present, is 
"script <file>", which executes a script in the same manner as described
above except from the console.
	
	
	
	
	
	
	
	
	
	
