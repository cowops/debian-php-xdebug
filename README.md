Debian-Php-Xdebug-Extension
===========================

Xdebug: A powerful debugger for PHP

Requirements
------------

This role requires a debian compliant system such as ubuntu.

Role Variables
--------------

debian:
    version: wheezy
xdebug:
    default_enable : 0,
    profiler_enable_trigger : 1,
    profiler_output_name : "cachegrind.out.%u",
    remote_enable : 0,
    remote_host : "80.11.76.108",
    max_nesting_level : 10000,
    profiler_output_dir : "/home/tmp/cachegrind/",
    trace_output_dir : "/home/tmp/cachegrind/",
    show_mem_delta : 1,
    trace_format : 1,
    var_display_max_data : 2048

Dependencies
------------

None

Example Playbook
----------------

    - hosts: servers
      roles:
         - { role: cowops.debian-php-xdebug, debian.version: wheezy, xdebug.default_enable : 0, xdebug.profiler_enable_trigger : 1, xdebug.profiler_output_name : "cachegrind.out.%u", xdebug.remote_enable : 0, xdebug.remote_host : "80.11.76.108", xdebug.max_nesting_level : 10000, xdebug.profiler_output_dir : "/home/tmp/cachegrind/", xdebug.trace_output_dir : "/home/tmp/cachegrind/", xdebug.show_mem_delta : 1, xdebug.trace_format : 1, xdebug.var_display_max_data : 2048 }

Tasks
-----

  - Install [xdebug](http://www.xdebug.org/docs/) php extension
  - Apply xdebug configuration

License
-------

BSD
