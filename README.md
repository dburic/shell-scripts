Shell scripts
======================================================================

This is a collection of shell scripts. The scripts have been developed,
tested and used with Bash on Linux, so they may not work with other shells
or systems.

This is a **work in progress**.

Licence
------------------------------

This software is distributed under the MIT license. See LICENSE for
details.

List of scripts
------------------------------

- jump      - quickly jump to a directory
- kwstart   - quickly start a file or URL via keyword
- onevim    - edit files using only one Vim instance
- par       - wrapper around xargs to allow easy execution of parallel jobs
- srename   - sequentially rename files
- start     - a file and URL starter/launcher

Installation
------------------------------

The installation procedure will overwrite files without asking, so be
careful.

Choose an installation directory, say `/usr/local`, and modify the variable
`LIBDIR` in `head.sh` so that it points to `/usr/local/lib/bash`. 

The variable `CONFIGDIR`, also in `head.sh`, contains the directory where
config files are kept. The default `$HOME/.scripts` can be changed to
any other directory.

Now execute the included setup script:

    ./setup prepare
    sudo ./setup --prefix=/usr/local install

If you have chosen `$HOME` as your installation directory and
`$HOME/.scripts` as your config directory, then you don't have to edit
`head.sh`, just execute the setup script:

    ./setup install

Executable files are copied to the `bin` subdirectory, while libraries are
copied to the `lib/bash` subdirectory of the chosen installation directory.

Configuration
------------------------------

By default, the scripts look for their config files in the directory
specified in the `CONFIGDIR` variable (see above). 

Examples of config files can be found in the `doc` directory.

Usage
------------------------------

Each script has a `--help` switch, which will print a help message with a
summary of the purpose of the script, a usage statement, a more elaborate
description, a list of available options, and some examples.

