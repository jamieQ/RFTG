This is a program to play Race for the Galaxy against AI or other human players.  Rules
for the game and expansions can be found at:

*	http://www.riograndegames.com/uploads/Game/Game_240_gameRules.pdf
*	http://www.riograndegames.com/uploads/Game/Game_253_gameRules.pdf
*	http://www.riograndegames.com/uploads/Game/Game_301_gameRules.pdf

### COMPILATION

A simple "./configure && make && make install" should suffice.  You
may need to install any development packages for libgtk.

To compile in order to run a multiplayer server, use "./configure --enable-server && make && make install". Running the server program also requires that mysql be installed and a database be configured. You can import the mysqldump file 'rftg.sql' to set up the requisite tables.

### RUNNING

Run with "./rftg".  You may specify number of players, expansion level,
etc with some command line options:

	-p <num>       -- Number of players (including yourself)
	-a             -- Play a two-player advanced game
	-e <expansion> -- Expansion level to play:
				0: Base game only
				1: The Gathering Storm
				2: Rebel vs Imperium

You may also change these setting once the game is running with the
"Select Parameters" option under the Game menu.

If you have compiled with the --enable-server option, you can launch the server program with "./server". It accepts the following options:

	-p <num>	-- Port number (deault is 16309)
	-d <string>	-- Database name (default is 'rftg')

### INTERFACE

Cards in your hand are displayed across the bottom of the window.  Your
active cards are just above, in the blue-shaded area.  Your opponents
active cards will be displayed in the top colored areas.

You may move your pointer over any card to see a full-sized version in
the upper-left.

In between your hand and active area is a prompt asking for your next
play.  Typically this is a request to choose a role, choose a card to
play or cards to discard, etc.  Select a role (or two roles if playing
the two-player advanced game) by using the drop-down box.  Select cards
to play or discard by clicking on them in your hand area.  When you
are satisfied, click the "Ok" button at the far right of the prompt
area.  This button will not be clickable if your current selection is
not legal.

### BUGS

If you encounter a bug, please open a github issue.

### LEGAL

The source code was originally created by [Keldon](http://keldon.net/) and is placed under the GPL.  For
details, see the file COPYING.

The original game of Race for the Galaxy was designed by Tom Lehmann and
published by Rio Grande Games.  Permission to distribute the card and
goal images has been granted by Rio Grande Games.
