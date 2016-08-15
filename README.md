# README #

Freeswitch config deployed with Ansible.

### Config Variables ###

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


### How do I get set up? ###

* Summary of set up
* Configuration
* Dependencies
* Database configuration
* How to run tests
* Deployment instructions

### Contribution guidelines ###

* Writing tests
* Code review
* Other guidelines

### Who do I talk to? ###

* Repo owner or admin
* Other community or team contact

### Freeswitch Config Layout ###
![fs_default_config.jpg](https://freeswitch.org/confluence/download/attachments/6587388/fs_default_config.jpg)
