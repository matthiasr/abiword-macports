Abiword/Macports
================

This was an attempt to get Abiword compiling through
MacPorts. Sadly, although it did compile, it didn't work for me; the
documents just wouldn't be rendered correctly. Since I didn't really
need it I abandoned the attempt at that point.

If you still want to try it out, here's what to do:

- if you haven't already, get & install [MacPorts](http://www.macports.org/)
- create the directory for the local portfile, clone the repository and build the portindex:
        mkdir -p ~/ports/editors
        git clone git://github.com/matthiasr/abiword-macports.git ~/ports/editors/abiword
        portindex ~/ports
- register it with MacPorts: add a new line 
        file:///Users/<your username>/ports
    to /opt/local/etc/macports/sources.conf right before
        rsync://rsync.macports.org/release/ports/ [default]
    (adjust the path suitingly)
- install cairo with the quartz variant
        sudo port install cairo +quartz
- install abiword
        sudo port install abiword

This should be it, AbiWord will be installed in /Applications/MacPorts.

Good Luck.
