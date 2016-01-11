Purpose
==========

This example adds a command to Trelis named `mbconvert`.  This command currently does nothing but write a message to the Trelis commandline console.

This example also adds a menu to Trelis with an entry to invoke `mbconvert`.  Rather than sending a Cubit command to the parser, the action on this menu item calls identical code to the new command.

This is accomplished by including the code in multiple places.

Dependencies
=============

This plugin/extension requires a licensed installation of Trelis 15.1.x and
the Trelis 15.1.x SDK.  The SDK should be untarred in the Trelis install
directory.

This plugin also depends on:
* libqt4-dev
* swig
* python2.7-dev

Build
======

```
mkdir bld
cd bld
cmake .. -DCMAKE_PREFIX_PATH=/path/to/Trelis-15.1/bin
make
```

Install
=======

Installation of the additional command is as simple as copying the generated
shared object library (`my_plugin.so`) to the Trelis plugin driectory:
`/path/to/Trelis-15.1/bin/plugins`.

