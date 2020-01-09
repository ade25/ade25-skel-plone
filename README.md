# About

This skeleton is a starting point for python3 based PLONE installations running with docker and using b5.

It can be used with b5-init to quickly start new projects.

On init a lot of stuff happens:

* download and build docker containers
* install build tools like npm or gulp
* install a python virtualenv and fabdeploit for deployment tasks
* install Plone using zc.buidlout
* ask you to edit the new projects config.yml
* create required configuration from templates
* setup Plone using default packages


# Install

## Install with b5-init (recommended)

```
b5-init -s <skeleton> <path>
```

where **skeleton** is a skeleton git repository (like this) and the **path** you want the project installed to.

For example:

```
b5-init -s git@github.com:ade25/ade25-skel-plone.git ~/plone/projects/new
```


During project init you will be asked to configure the project's config.yml.

## Clone and run (for dev)

First clone this repository and change into it's path. then run:

```
b5 --run-path init --config config.yml --config config.init.yml --config config.local.yml project:init
```

Note how this uses init/ as run-path for b5 and then calls the project:init task.

```bash
b5 install
vi build/config.local.yml
b5 update
```

# Running the project

As with every other docker and b5 project:
Start the containers with **b5 run** or **b5 run -d** for running in background.

```bash
b5 run
```

# Housekeeping

To update the project:

```bash
b5 update
```

# Notes

TODO: Add some special notes about the project
