% PDSHELL(1) pdshell <version>
% Bruno F. Fontes \<developer@brunofontes.net\>
% <date>

# NAME
pdshell - a pomodoro timer in the shell

# SYNOPSIS
**pdshell** [*\--install*|*\--uninstall*]\
**pdshell** [*\--edit-config*]\
**pdshell** \[*-c*|*\--config*\] config-file ...

**pdshell** \[\[*-s*|*\--song*\] path|music-file\] \
\ \ \ \ \ \ \ \ \ \[\[*command-options*\] shell-command\] ...


# DESCRIPTION
**pdshell** is customizable pomodoro tool that allows you to specify any script or command to run at start and/or end of pomodoros, short and/or long breaks. You can also specify the music player and even the alarm player, so it can work exactly the way you need it.

## Commands
Commands can be specified as a regular bash command that will be run in background. You can have as many commands as you need, by repeating the parameter. Example:

\ \ \ **pdshell** *\-ssbc* "firefox https://brunofontes.net" \
\ \ \ \ \ \ \ \ \ \ \ *\-ssbc* "gomuks" *\-ssbc* "myscript.sh"

If no "end command" is specified, all commands will be killed at the end of the timer. In our example, **firefox**, **gomuks** and **myscript.sh** would be killed when the short break were over. On the other side, if an "end command" is specified, you will need to handle (or not) to stop your commands.

## Enrionment variables
When running scripts from **pdshell**, the following envionment varibles are available:

**\$PDSHELL_SESSIONS**
: The defined number of sessions before a long break.

**\$PDSHELL_SESSION**
: The number of the active session starting from 1, up to *\$PDSHELL_SESSIONS*.

## Keyboard Control
**m**
: Toggles *music* on or off.

**n**
: *Next* section. It actually forwards the current pomo/pause to the very last second.

**p**
: *Pause* the pomodoro. To continue, press **ENTER** at any time. The pomodoro will be restarted.

**q**
: *Quit* **pdshell**.

**r**
: *Restarts* pomodoro.

**R**
: *Reload* the config file.

## Config file
All parameters can be defined in a config files, so you can run \'**pdshell**\' to load the default config file or \'**pdshell** *-c* CONFIG_FILE\' to specify a different one.

Run \'**pdshell** *\--edit-config*\' to see/edit the config file.

# OPTIONS
**-t**, **\--time** *MINUTES*
: Duration, in minutes, of each pomo. [Default: 25]

**-d**, **\--delay** *MINUTES* 
: Duration, in minutes, of the short break. [Default: 5]

**-ld**, **\--long-delay** *MINUTES*
: Duration, in minutes, of the long break. [Default: 30]

**-n** *INT*
: Number of sessions before a long break. [Default: 4]

**-f**
: Shows timer using *Figlet* (you need to have *figlet* installed to use this option)

**-m**, **\--music**
: Enables music during pomos (default).

**-nm**, **\--no-music**
: Disables music during pomos.

**\--player** *PLAYER_CMD*
: Define a custom player. It will be used for the music and also the alarm, if not specified an specific one. [Default: */usr/bin/play -q*]

**\--alarm-player** *PLAYER_CMD*
: Specify a different player for the alarm. Usefull if you just want to have a different volume or output for it. [Default: same as *\--player*]

**-s**, **\--song** *PATH*|*FILE*
: Specify a folder to randomicaly play all musics or a music file to play it directly. You can also define *\--player* as **mpv** and a **YouTube** video URL here. If you need a more advanced/personalized way, set **\--no-music** parameter and include a **\--start-cmd** with it. [Default *$HOME/Music*]

**-c**, **\--config** *FILE*
: Specify a different configuration file to be used. You can save it on *\$XDG_CONFIG_HOME* or, if not defined, *$HOME/.config* to be specified by just the name (without the path).

**-nc**, **\--no-config**
: Ignores the default config file so you can run it with the default settings. Can be combined with any parameters.

**\--edit-config**
: Edit the default config file using your default *$EDITOR* and exit.

**-sc**, **\--start-cmd** *COMMAND*|*SCRIPT*
: Define a command to run at the start of a pomodoro. Multiple commands can be used by adding the parameter again.

**-ec**, **\--end-cmd** *COMMAND*|*SCRIPT*
: Define a command to run at the end of a pomodoro. Multiple commands can be used by adding the parameter again.

**-ssbc**, **\--start-short-break-cmd** *COMMAND*|*SCRIPT*
: Define a command to run at the start of a short break. Multiple commands can be used by adding the parameter again.

**-esbc**, **\--end-short-break-cmd** *COMMAND*|*SCRIPT*
: Define a command to run at the end of a short break. Multiple commands can be used by adding the parameter again.

**-slbc**, **\--start-long-break-cmd** *COMMAND*|*SCRIPT*
: Define a command to run at the start of a long break. Multiple commands can be used by adding the parameter again.

**-elbc**, **\--end-long-break-cmd** *COMMAND*|*SCRIPT*
: Define a command to run at the end of a long break. Multiple commands can be used by adding the parameter again.

**\--install**
: Install **pdshell** so you can run it from anywhere and exit.

**\--uninstall**
: Removes installed **pdshell** and exit.

**-h**, **\--help**
: Shows a help message and exit.

# EXAMPLES
**pdshell \--player "/bin/mpv \--no-vid \--volume=50.000"**
: Play the music using `/bin/mpv` with no video and volume set as 50%.

**pdshell -nm -sc "tmux splitw todolist list" -sc "firefox https://webmail.company.com" -sc "./logHour.sh"
: At the start of each pomo it will split the tmux window, and list tasks on `todolist` at it, open the company webmail in **firefox** and run a script called **logHour.sh*.

# EXIT VALUES
Exit Values: The possible return codes and their meanings.

# BUGS
Bugs: A list of known bugs and quirks. Sometimes, this is supplemented with (or replaced by) a link to the issue tracker for the project.

# AUTHOR
Author: The person or people who wrote the command.

# COPYRIGHT
Copyright: Your copyright message. These also usually include the type of license under which the program is released.
