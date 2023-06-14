kubealex.general.role_generate_ca
=========

The `role_generate_ca` role creates a custom Certificate Authority (CA) for self-signing certificates.

Requirements
------------

- `community.crypto.openssl_privatekey`: This module requires the `pyOpenSSL` package.
- `community.crypto.openssl_csr_pipe`: This module requires the `pyOpenSSL` package.
- `community.crypto.x509_certificate`: This module requires the `cryptography` package.

Role Variables
--------------

| Variable              | Description                                | Default Value   |
|-----------------------|--------------------------------------------|-----------------|
| `ca_key_passphrase`   | Passphrase for the CA private key           | `mypassphrase`  |
| `ca_filename`         | Filename of the CA certificate              | `ca_cert`       |
| `ca_destination_path` | Destination path for the CA certificate     | `~/generated-certs` |
| `ca_cn`               | Common Name (CN) for the CA certificate     | `Self Signed CA` |
| `ca_C`                | Country Name (C) for the CA certificate     | `US`            |
| `ca_L`                | Locality Name (L) for the CA certificate    | `Galaxy`        |
| `ca_O`                | Organization Name (O) for the CA certificate | `My Company`   |
| `ca_OU`               | Organizational Unit Name (OU) for the CA certificate | `My Lab`    |
| `archive_ca`          | Flag indicating whether to create an archive of the CA certificate | `false` |


Dependencies
------------

N/A

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    ---
    - name: Test role
      hosts: localhost
      roles:
        - kubealex.general.role_generate_ca


License
-------

Apache 2.0

Author Information
------------------

Alessandro Rossi <al.rossi87@gmail.com>