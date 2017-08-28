generic motd
=========

[![Build Status](https://travis-ci.org/ANTS-Framework/generic_motd.svg?branch=master)](https://travis-ci.org/ANTS-Framework/generic_motd)

Manage the message of the day file to display the following message:

```


        This system is managed by {{ generic_motd__support_name }} via

                            ___    _   _____________
                           /   |  / | / /_  __/ ___/
                          / /| | /  |/ / / /  \__ \ 
                         / ___ |/ /|  / / /  ___/ / 
                        /_/  |_/_/ |_/ /_/  /____/  
                                                    

                    Framework for Linux and macOS clients

       Please do not hesitate to contact us if you have any question
       Mail: {{ generic_motd__support_mail }}                      Tel: {{ generic_motd__support_tel }}
```

Role Variables
--------------


```yml
generic_motd__template: 'motd.j2'
generic_motd__support_name: 'Support Unit'
generic_motd__support_tel: 'to be replaced'
generic_motd__support_mail: 'to.be@replaced.ch'
```

Example Playbook
----------------


```yml
    - hosts: all
      vars:
        - generic_motd__support_name: "Pretendcorp Unit One"
        - generic_motd__support_tel: "123 123 123"
        - generic_motd__support_mail: "support@pretendcorp.com"
      roles:
         - generic_motd

    # Use your own motd template
    - hosts: vip
      vars:
        - generic_motd__template: /path/to/template.j2
      roles:
         - generic_motd
```

License
-------

GPLv3

Author Information
------------------
Part of the [ANTS Framework](https://ants-framework.github.io/)
