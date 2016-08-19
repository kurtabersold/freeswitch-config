freeswitch-config
=================

Freeswitch config deployed with Ansible.

Requirements
------------

Any pre-requisites that may not be covered by Ansible itself or the role should be mentioned here. For instance, if the role uses the EC2 module, it may be a good idea to mention in this section that the boto package is required.

Role Variables
--------------

A description of the settable variables for this role should go here, including any variables that are in defaults/main.yml, vars/main.yml, and any variables that can/should be set via parameters to the role. Any variables that are read from other roles and/or the global scope (ie. hostvars, group vars, etc.) should be mentioned here as well.

Default variables are displayed, override as needed.


General variables
```
freeswitch_path: /usr/local/freeswitch #Path to the FreeSwith directory
freeswitch_owner: freeswitch
freeswitch_group: daemon
```

Client Credential Related
Used in `conf/vars.xml`, `conf/directory/default/`
```
credentials:
  default:
    password: "1234"
```

Used in: `conf/sip_profiles/external/flowroute.xml`
```
gateway:
  flowroute:
    auth_username: "TECH_PREFIX"
    password: "SIP_PASSORD"
    proxy: "sip.flowroute.com"
```

Used in `conf/dialplan/public/01_flowroute_inbound_did.xml`
```
inbound_did:
  flowroute:
    did01:
      number: "+15555551212"
      extension: "1001"
```

Dependencies
------------

A list of other roles hosted on Galaxy should go here, plus any details in regards to parameters that may need to be set for other roles, or variables that are used from other roles.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: username.rolename, x: 42 }

License
-------

BSD

Author Information
------------------

An optional section for the role authors to include contact information, or a website (HTML is not allowed).

Freeswitch Config Layout
------------------------

![fs_default_config.jpg](https://freeswitch.org/confluence/download/attachments/6587388/fs_default_config.jpg)
