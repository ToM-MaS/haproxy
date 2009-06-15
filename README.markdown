HAProxy
=======

These are just some scripts that are used to split up the monolithic configuration file of haproxy into chunks.

haproxy-config.py
-----------------

This is a python script that merges the configuration of haproxy which is layed out in a defined directory structure. It is intended to be run inside an init script.

This script expects a fixed directory structure. For more information about that have a look into the comments on top of the script.

haproxy-init
------------

This script is an example init script for haproxy. It is adapted from the script which is provided by the [haproxy package for debian](http://packages.debian.org/lenny/haproxy). The original author of the script is Arnaud Cornet.


Getting started
---------------

1. Copy `haproxy-config` into a directory of your choice. I recommend something like `/usr/local/sbin/haproxy-config`
2. Copy haproxy-init into your `/etc/init.d` directory. You should rename it to something like `haproxy`.
3. Adjust the variables on top of the init script to match your local installation.
4. Run `chmod +x /etc/init.d/haproxy /usr/local/sbin/haproxy-config.py` (adjust as needed)