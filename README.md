irssi-hilite
============

Enables to receive desktop notifications from remote Irssi box. Uses `netcat` to listen (port 6667) for notifications from remote Irssi installaton over SSH. Currently has notifications for regular highlight, private message and DCC.

## Installation
### Remote
Copy `notify.pl` to `~/.irssi/scripts/` folder located in the remote Irssi box. To avoid loading the script every time add this to the `autorun` directory.

```
cd ~/.irssi/scripts/autorun/
ln -s ../notify.pl
```
To start the script insert `/script load notify` command or restart Irssi.

### Local
Copy remaining files to a preferred location (e.g. `~/bin/`) on your local machine and make sure `irssi` is exported to the path.
*NB!* Rename `irssi` if needed to avoid possible conflicts with the program itself.

## Usage
Enter `irssi username@host` to start `netcat` and initialise the SSH session to the remote Irssi box.


### Credits
Irssi script based on [Irssi notify for Desktop Notify](https://github.com/tbaumann/Irssi-nofity-for-Desktop--Notify).
[Shell script for killing subprocesses](http://www.unix.com/17971-post5.html)
