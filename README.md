Raspberry Headless Setup
=========

Sets up a Raspberry Pi for headless use.
It disables audio and swap, sets up the hostname, default locale and default timezone.
It also sets up some directories with frequent file writing to use tmpfs.


Requirements
------------

A Raspberry Pi.

Role Variables
--------------

* system_locale: "en_US.UTF-8"
* system_timezone: "Europe/Paris"
* system_tmpfs_mounts: list of filesystems to set up
  - { src: "/run", size: "10%", options: "nodev,noexec,nosuid" }
  - { src: "/tmp", size: "10%", options: "nodev,nosuid" }
  - { src: "/var/log", size: "10%", options: "nodev,noexec,nosuid" }


Dependencies
------------

None.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - ansible-raspberry-headless

License
-------

Unlicensed.
