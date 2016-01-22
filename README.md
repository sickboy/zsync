# zsync

fork of http://zsync.moria.org.uk/zsync.git with bugfixes and support for libcurl

This fork addresses:

* Reimplemented http authentication support [WARN: the current implementation should send your auth details also to redirected servers - by design]
* Reimplemented realtime progress reporting
* Disabled 'no_progress' when no tty detected

#### [Download](http://zsync.moria.org.uk/downloads)

Current Version: [zsync-0.6.2.tar.bz2](http://zsync.moria.org.uk/download/zsync-0.6.2.tar.bz2)

To install, it is the usual configure, make, make install sequence —<br />
see the INSTALL file for step-by-step instructions.<br />
You do not have to install zsync if you are just trying it out, as both zsync and zsyncmake require no data files installed; installation just puts the programs and manual pages into the normal paths on your system.


#### In-development & Source Code History
zsync history is kept in a git repository. You can get a copy of the history with:

git clone http://zsync.moria.org.uk/zsync.git


### To build

(on cygwin for some reason must add #include <sys/select.h> before #include <sys/types.h> in include/curl/curl.h)

aclocal
autoheader
automake --force-missing --add-missing
autoconf
./configure
make
