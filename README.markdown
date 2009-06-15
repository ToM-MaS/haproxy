HAProxy
=======

This are just some scripts that are used to split up the monolithic configuration file of haproxy into chunks.

haproxy-config
--------------

This is a python script that merges the configuration of haproxy which is layed out in a defined directory structure. It is intended to be run inside an init script.

haproxy-init
____________

This script is an example init script for haproxy. It is adapted from the script which is provided by the [haproxy package for debian](http://packages.debian.org/lenny/haproxy). The original author of the script is Arnaud Cornet.


Getting started
---------------

1. Copy `haproxy-config` into a directory of your choice. I recommend something like `/usr/local/sbin/haproxy-config`
2. copy haproxy-init into your `/etc/init.d` directory. You should rename it to something like `haproxy`
3. Adjust the variables on top of the init script to match your local installation.