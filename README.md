**akin-ozer.ansible_role_ssl**
=========

Creates self signed SSL certificate for given host.

**Requirements**
------------

Pip is required on ansible machine. "pyOpenSSL" pip package is also required. "python-setuptools" is also required for pip. 

**Role Variables**
--------------

`server_hostname` is required. This is basically Common Name for the certificate.
`key_output_path` is directory name for the certificate files. Default is "/tmp".

**All the defaults:**
```
key_size: 2048
key_type: RSA

key_output_path: /tmp

country_code: US
organization_name: ssl-demo
email_address: info@ssl-demo.com
```

**Dependencies**
------------

No role dependencies.

**Example Playbook**
----------------

    - hosts: servers
      roles:
         - { role: akin-ozer.ansible_role_ssl, server_hostname: example.com }

**License**
-------

MIT/BSD

**Author Information**
------------------

This role was created in 2020 by [Akın Özer](https://github.com/akin-ozer).