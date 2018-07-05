Ansible Role - macOS Certificates
=========

This role is meant to install and trust certificates on macOS. It should work
both via ansible-pull or regular ansible if the mac has SSH enabled.

Requirements
------------

* macOS 10.9+

Role Variables
--------------

This role expects that after you install it into your project that you copy the
certificates you want to install into the `files` directory. Then in your
variable list you can list which ones you want installed and trusted.

    certificates:
      - certone.cer
      - certtwo.cer

Example Playbook
----------------

    - hosts: localhost
      vars:
        certificates:
          - certone.cer
          - certtwo.cer
      roles:
        - knightsc.ansible-role-macos-certificates

License
-------

MIT

Author Information
------------------

[Scott Knight](https://github.com/knightsc)
