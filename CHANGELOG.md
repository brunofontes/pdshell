## 0.1.3 (outubro 20, 2022)
  - fix: forloop working again
  - feat: added pause command

## 0.1.2 (agosto 23, 2022)
  - feat: DEBUG messages added if used proper variable
  - feat: alarm now also notify-send a message
  - feat: added a simple logger
  - fix: commands are working again
  - feat: added shotcut to stop/start music
  - fix: start command now ends again - refactor variables
  - feat: improved configuration loader by filename (close #3)
  - feat: added alarm player configuration - close #8
  - refactor: added function to run commands
  - refactor: renamed variable $2 to SESSION
  - fix #2: pausing a pomodoro now also pauses the music
  - docs: padronizing caps on help
  - sec: improved shebang security
  - fix: autocomplete is working with the full commands again
  - feat: added audio player configuration (#1)
  - feat: autocomplete now supports -c, -s and commands parameters

## 0.1.1 (junho 23, 2022)
  - feat: added autocomplete file
  - feat: added option to reload configuration
  - fix: pomo shortcuts working again

## 0.1.0 (junho 12, 2022)
  - feat: added configuration for long break
  - fix: short and long break ends now run when exiting app
  - fix: end short break cmds now working
  - feat: implemented all parameters in sample config file
  - feat: implemented long-break command
  - docs: added info about -nc parameter
  - feat: emit warning if alarm.wav file were not present
  - feat: added option to ignore the config file
  - fix: it now respect the XDG_CONFIG_HOME if exists
  - fix: does not show error messages when playing songs
  - feat: added install and uninstall options
  - docs: including music information in docs
  - fix: single music file not always playing
  - fix: music is playing again
  - feat: added break shortcuts with instructions
  - feat: added personalyzed shortcut during pomodoro
  - feat: added option for personalized shortcut during pomo
  - fix: start commands and break commands are killed automatically again
  - fix: alarm is playing again
  - feat: added shortcuts to use during the pomodoro
  - fix: alarm and music now work when pdshell is on any folder
  - fix: single player being used: aplay
  - feat: added more cli parameters
  - fix: cli parameters working again
  - fix: Cmds now run even if music is off
  - fix: removed very personal option
  - fix: default short break time is now 5 minutes
  - feat: config file now has better default options
  - feat: added option to install config file
  - feat: added config file
  - feat: start command can be used multiple times at once
  - docs: old logo removed
  - docs: Improving README.md file
  - fix: Fixing file permission
  - style: Renaming tool
  - docs: Improved README.md file
  - docs: Added license information
  - feat: adding a bunch of stuff

## 0.0.1
  - Testing a few updates
  - Merge pull request #2 from LytixDev/fix-paplay
  - starts paplay with specific name, so it can be terminated locally
  - improved portability (#1)
  - made script more bash like
  - Added example to README
  - Figlet mode improved
  - Create README.md
  - added logo
  - improved figlet mode
  - more robust error handling and consistent naming
  - added automatic audio play and pause with cmus
  - added alarm sound
  - consistent space use
  - added font awesome and emoji sugar
  - fixed exit bug and added figlet mode
  - removed cursor, added SIGINT handling and improved core feature
  - oopsie
  - initial commit

