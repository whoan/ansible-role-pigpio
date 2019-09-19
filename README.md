Pigpio
=========

An Ansible Role that installs any version (provided by param) of [pigpio library](http://abyz.me.uk/rpi/pigpio/) on a Raspberry Pi.

Find the role in [Ansible Galaxy](https://galaxy.ansible.com/whoan/pigpio).

Requirements
------------

You should uninstall any previous version of `pigpio` in your environment, if any.

Role Variables
--------------

These are the role variables (and its default values):

```
pigpio_version: master
threads_for_make: "{{ ansible_facts['processor_vcpus'] }}"
```

> `ansible_facts['processor_vcpus']` is the same as the value of `nproc`.

Dependencies
------------

None.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: <you_raspberry_ip>

      tasks:
      - import_role:
          name: whoan.pigpio

License
-------

[MIT](http://mths.be/mit)
