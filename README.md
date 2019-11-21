raspi-makestaticip
=========

A fresh out of the box Raspberry Pi wants to dhcp to get its address.
Obviously if the plan is to run it as the only dhcp server on the network,
this is not a sound plan.

This role takes whatever the Pi got from the dhcp server and changes
/etc/dhcpcd.conf so that it will get that address in the future without
a dhcp server around.

Tests with 2019-09-26-raspbian-buster-lite.img suggest that hand-editing this file,
even changing subnets, even moving the SD card to another Pi (all of which are
in the interests of putting the staged Pi into production) is A-OK.


Requirements
------------

none

Role Variables
--------------

none - will be some in the next iteration or three

for your requirements.yml:

- src: https://github.com/res3066/ansiblerole-raspi-makestaticip
  name: raspi-makestaticip
  scm: git


Dependencies
------------

none

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - raspi-makestaticip

License
-------

MIT

Author Information
------------------

Rob Seastrom <rs@seastrom.com>

