blinky - Blink the keyboard's led on notifications
==================================================

## What is it?

This small shell script will blink a keyboard's led (Scroll Lock by default) every time a notification is shown.

Just clone the repo/download the script and try this:

```sh
./blinky &

notify-send "Hello blinky"
```

## Why?

[zbell](http://blog.patshead.com/2014/01/getting-notified-when-long-running-zsh-processes-complete.html)
is a very useful script.
However, when I put my terminal window on fullscreen (those extra columns), it's nearly impossible to see those notifications.
Scroll Lock is a nearly useless button so why not make it more useful?

## Options

* `-l=, --lock-file=<lock-file>`: Specify a lock file to ensure only one instance of blinky is running. (Default: `/tmp/blinky.lock`)
* `-p=, --pid-file=<pid-file>`: Specify a file to write blinky's pid to. (Default: `/tmp/blinky.pid`)
* `-i=, --interval=<interval>`: Blinking interval in seconds. (Default: 1)
* `-n=, --led-name=<led-name>`: Name of the led to blink. (Default: `"Scroll Lock"`)
* `-k, --kill`: Kill the current running blinky instance whose pid is stored in the specified pid file.
