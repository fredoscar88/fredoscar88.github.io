MSPLite (name pending) Alpha 1.0-
MSPLite runs only on minecraft servers. Command blocks are
automatically placed into the world by communicating with the server.

How to use
**You will need a 1.9 snapshot (15w47c as of now is the latest), a minecraft server jar file (same snapshot!), and a pregenerated world**
	
	I- Running MSPLite	
		1. 	Place all of the files that came in the .zip folder into
			the same directory you put the server jar file.
		
		2.	Rename the server jar file to "server.jar".
		
		3.	Double click "MSPRun" or "MSPRun.bat" to launch MSPLite.
			If you have done everything correctly it should start the server (it may take a moment)

			
	II- Writing the redstone text files
		1.	All redstone text files are stored in the Redstone directory.
			By default, this is a folder called "Redstone". You can enter in
			"MakeRedstone" into the MSP terminal that opens up to generate this
			file if it doesn't exist.
		
		2.	To start writing, create a new textfile inside of the redstone
			directory. In the first line write ":NEW SET"
			Every line after that (with some exceptions) is
			put into a command block, which executes in the order commands
			are listed in the file. There is other syntax you can use to generate
			more complicated redstone
			
			2b.	Follow the syntax guide in the "advanced readme" text file for
				help with advanced usage of MSPLite
							
		3.	You cannot name redstone text files the following:
			-"documentation.txt"
			-"NOTES.txt"	(or "notes.txt")
			-"replaces.txt"
			-output.txt
			Note: It helps if you have file extensions visible
	
	
	III- Generating the redstone
		1.	If you're satisfied with your text file(s), save it/them.
			
		2. 	In the console that opened when you ran "MSPRun.bat", 
			enter in "MakeRedstone". The first time redstone is generated after 
			MSPLite is started may take a moment to work.
			
**Lastly if you have any questions or you think this readme did a bad job, contact me
on github (fredoscar88), the minecraft forums (fredoscar88), or over skype (if Im a contact)!**
-Thanks, -fredo

FOR ADVANCED INFORMATION PLEASE SEE THE ADVANCED README