# Pomodoro timer in the shell

> A fork of https://github.com/LytixDev/tomatoshell

## Why?

I've downloaded tomatoshell for my personal use and missed one or other detail
that was very personal and it would not be interesting for the main tool.

After a few month of using it, I noticed it was getting a different 
direction than the original tool and I was interesting in adding more
functionalities and letting it open to interact with other tools.

## Requirements: 
- figlet: for -f figlet mode on text
- play (sox): for playing local music

## How to install:
```
$ git clone https://github.com/brunofontes/pdshell
$ cd pdshell
$ ./pdshell --install
```

## How to use:
`$ pdshell`

You can use cmd parameters or change the configuration file to personalize.
As default, it will play any mp3 files under `$HOME/Music`

## Shortcuts

During a pomodoro, you can use the following shotcuts:

```
r - reset a pomodoro
p - pause the pomodoro (it restart the pomo afterwards)
n - (temporary) advance to the last second of the actual pomo
q - quit
```


## Usage
```
-t,    --time,                  time for every session in minutes [default:25 minutes]
-d,    --delay,                 delay between sessions in minutes [default:5 minutes]
-m,    --music,                 enable the music
-nm,   --no-music,              disalbe the music
-n,                             total sessions [default:4]
-f,                             figlet on
-s,    --song,                  choose a mp3 file or a folder of mp3s to play during each session

-c,    --config,                read an alternative config file
-nc,   --no-config,             ignore the default config file

-sc,   --start-cmd,             *bash command that will run at the start of a pomodoro
-ec,   --end-cmd,               *bash command that will run at the end of a pomodoro

-ssbc, --start-short-break-cmd, *bash command that will run at the start of a short break
-esbc, --end-short-break-cmd,   *bash command that will run at the end of a short break

-slbc, --start-long-break-cmd,  *bash command that will run at the start of a long break
-elbc, --end-long-break-cmd,    *bash command that will run at the end of a long break

       --install,               Install the program to be run from anywhere
       --uninstall,             Uninstall the program

-h,    --help,                  shows this help
```

* You can add multiple commands by including the prefix again. Example:
pdshell -sc \"play ~/music.mp3\" -sc \"myscript.sh\"

Example 1:
`./pdshell -n 2 -s ~/Music/song.mp3 -t 30`

This will start the program with two sessions, play the song given during 
the session, and each session lasts for 30 minutes.

Example 2:
`./pdshell -sc "/bin/mpv --vid=no https://www.youtube.com/watch?v=AiH9LG22zW4"`

This will start a regular pomodoro, but playing the YouTube video in the background using MPV.


## Objectives

- Make it easy for the user to run one or more of their personal commands 
  at the start or end of pomodoros, short breaks and long breaks
- Make it possible to play local or online songs, randomly or not
- Follow the Pomodoro technich rule: a pomodoro cannot be interrupted


## Contributing

If you find this interesting and want to help organizing and buildint
it, just:

- Fork it and get in touch!

I will be happy to have some help improving the tool!
