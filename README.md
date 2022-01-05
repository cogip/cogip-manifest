## Pre-requisites ##

This documentation supports Ubuntu 20.04 LTS version.
However command listed below should work with any recent debian-like Linux
distribution.

### git ###

From https://git-scm.com/:
Git is a free and open source distributed version control system designed to
 handle everything from small to very large projects with speed and efficiency.

To install git:

```bash
  $ sudo apt install git
```

For more informations: https://git-scm.com/

### repo ###

From https://gerrit.googlesource.com/git-repo/:
Repo is a tool built on top of Git. Repo helps manage many Git repositories,
does the uploads to revision control systems, and automates parts of the
development workflow. Repo is not meant to replace Git, only to make it easier
to work with Git. The repo command is an executable Python script that you can
put anywhere in yoaur path.

To install repo:

```bash
  $ mkdir ~/.bin
  $ echo "PATH=~/.bin:\$PATH" >> ~/.bashrc && source ~/.bashrc
  $ curl https://storage.googleapis.com/git-repo-downloads/repo > ~/.bin/repo
```

For more informations: https://gerrit.googlesource.com/git-repo/+/refs/heads/master/README.md

## Get the project ##

### Full project ###

To get the COGIP full source tree :

```bash
  $ mkdir cogip/ -p && cd cogip/
  $ repo init -u git@github.com:cogip/cogip-manifest.git -m cogip-manifest.xml
  $ repo sync
```

#### yocto-build project ####

The yocto-build project is the Yocto linux distribution installed on robot
MPU board.

Refer to `cogip/yocto-build/README.md` for more information.

To get the COGIP pi project source tree only:

```bash
  $ mkdir cogip/ -p && cd cogip/
  $ repo init -u git@github.com:cogip/cogip-manifest.git -m cogip-pi.xml
  $ repo sync
  $ cd yocto-build/
```

#### mcu-firmware project ####

The mcu-firmware project is the firmware flashed on robot MCU board.

To get the COGIP mcu-firmware project source tree only:

```bash
  $ mkdir cogip/ -p && cd cogip/
  $ repo init -u git@github.com:cogip/cogip-manifest.git -m cogip-mcu-firmware.xml
  $ repo sync
  $ cd mcu-firmware/
```

Refer to `cogip/mcu-firmware/README.md` for more information.

#### simulation project ####

The simulation project is the source code of simulator and co-pilot application.


To get the COGIP mcu-firmware project source tree only:

```bash
  $ mkdir cogip/ -p && cd cogip/
  $ repo init -u git@github.com:cogip/cogip-manifest.git -m cogip-simulation.xml
  $ repo sync
  $ cd simulation/
```

Refer to `cogip/simulation/README.md` or https://cogip.github.io/simulation for more information.
