# osc-tui

Designed to be a POC of a Outscale's Cockpit inside the terminal using curses.<br/>The officially supported python version is currently 3.<br/> The code is currently a bit dirty... Maybe big changes are coming!<br>To refresh any table, press [F5].<br>Feel free to suggest oher architectures, libs...<br/>The `src/` folder contains the project's sources.<br/>The ```tests/``` folder contain some crappy code used to test API calls or any other things...

# Installation

You will need to install python3:<br>

* Python3 (https://www.python.org/downloads/).

## Clone, setup, build and install:

* `curl https://raw.githubusercontent.com/outscale-dev/osc-tui/master/setup.sh | bash -s -- -y`

## Clone and setup only:

* `curl https://raw.githubusercontent.com/outscale-dev/osc-tui/master/setup.sh | bash -s -- -n`

# Running the client.

## If installed:

* `osc-tui`

## If not installed (for devs):

Move to the osc-tui folder, then run:

* `source env/bin/activate`to activate the virtual env.
* `python3 osc_tui/main.py`

Then you can deactivate the virtual env:

* `deactivate`

# Packaging the app with pip (BETA, WIP).

We will need to rename some imports so we have a script for that: `configure.sh`.<br>
This script is ran by the `setup.py`to move in `--release`config.<br>
If you want to be able again to run directly the python file, you will have to do first:
* `./configure.sh --dev`
It will rename back all imports.


Finally build and install the package:<br>

* `sudo python3 setup.py build install`

# Contributing

Just a few rules:<br>
* Format correctly your code (you can do `autopep8 --in-place --aggressive --aggressive osc_tui/*.py`).
* Add external dependencies as less as possible.


