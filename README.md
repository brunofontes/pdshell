# Pomodoro timer in the shell

> A fork of https://github.com/LytixDev/tomatoshell

## Why?

I've downloaded tomatoshell for my personal use and missed one or other detail
that was very personal and it would not be interesting for the main tool.

After a few month of using it, I noticed it was getting a different 
direction than the original tool and I was interesting in adding more
functionalities and letting it open to interact with other tools.

## Requirements: 
- figlet (for -f figlet mode on text)
- aplay (for playing local music)

## How to use:
```
$ git clone https://github.com/brunofontes/pdshell
$ cd pdshell
$ ./pdshell
```

## Options
```
-t,  --time,          time for every session in minutes [default:25 minutes]
-d,  --delay,         delay between sessions in minutes [default:5 minutes]
-m,  --music,         chose song for 'play' to play during each session
-n,                   total sessions [default:4]
-f,                   figlet on
-s,  --song,          full path to song or command
-o,  --oxo,           locks the OXO KDE Activity in place during sessions
-sc, --start-cmd,     bash command that will run at the start of a pomodoro
-ec, --end-cmd,       bash command that will run at the end of a pomodoro
-pc, --pause-cmd,     bash command that will run at the start of a break
-epc,--end-pause,cmd, bash command that will run at the end of a break
-h,  --help,          shows this"
```

Example 1:
`./pdshell -n 2 --music ~/Music/song.mp3 -t 30`

This will start the program with two sessions, play the song given during 
the session, and each session lasts for 30 minutes.

Example 2:
`./pdshell --song "/bin/mpv --vid=no https://www.youtube.com/watch?v=AiH9LG22zW4"`

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
