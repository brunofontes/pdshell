% PDSHELL(1) pdshell <version>
% Bruno F. Fontes \<developer@brunofontes.net\>
% <date>

# NAME
pdshell - a pomodoro timer in the shell

# SYNOPSIS
**pdshell**\
**pdshell** [*\--install*|*\--uninstall*]\
**pdshell** [*\--edit-config*]\
**pdshell** \[*-c*|*\--config*\] config-file ...

**pdshell** \[\[*-s*|*\--song*\] path|music-file\] \
\ \ \ \ \ \ \ \ \ \[\[*command-options*\] script|command\] ...


# DESCRIPTION
**pdshell** is customizable pomodoro tool that allows you to specify any script or command to run at start and/or end of pomodoros, short and/or long breaks. You can also specify the music player and even the alarm player, so it can work exactly the way you need it.

## Commands
Commands can be specified as a regular bash command that will be run in background. You can have as many commands as you need, by repeating the parameter. Example:

\ \ \ pdshell \-ssbc "firefox https://brunofontes.net" \
\ \ \ \ \ \ \ \ \ \ \ \-ssbc "gomuks" \-ssbc "myscript.sh"

If no "end command" is specified, all commands will be killed at the end of the timer. In our example, **firefox**, **gomuks** and **myscript.sh** would be killed when the short break were over. On the other side, if an "end command" is specified, you will need to handle (or not) to stop your commands.

## Keyboard Control
**m**
: Toggles *music*.

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

# OPTIONS
**-t**, **\--time** *MINUTES*
: Duration, in minutes, of each pomo. [Default: 25]

**-d**, **\--delay** *MINUTES* 
: Duration, in minutes, of the short break. [Default: 5]

**-ld**, **\--long-delay** *MINUTES*
: Duration, in minutes, of the long break. [Default: 30]

**-n** *INT*
: Number of sessions before a long break. [Default: 4]

# EXAMPLES
Examples: Some examples of common usage.

# EXIT VALUES
Exit Values: The possible return codes and their meanings.

# BUGS
Bugs: A list of known bugs and quirks. Sometimes, this is supplemented with (or replaced by) a link to the issue tracker for the project.

# AUTHOR
Author: The person or people who wrote the command.

# COPYRIGHT
Copyright: Your copyright message. These also usually include the type of license under which the program is released.
