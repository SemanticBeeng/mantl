Vault
=====

.. versionadded:: 0.3.0

`Vault <https://vaultproject.io/>`_ "secures, stores, and tightly controls
access to tokens, passwords, certificates, API keys, and other secrets in modern
computing." It is currently included as a technology demo in
Mantl.

Variables
---------

.. data:: vault_default_port

   Port for Vault to listen on

   default: ``8200``

.. data:: vault_command_options

   Extra options to pass to Vault at startup

   default: ``-insecure``

.. data:: vault_config_file

   Where to store the Vault configuration file

   default: ``/etc/vault/vault.hcl``

.. data:: vault_addr

   The default advertised address for vault, i.e. where Vault will listen.

   default: ``vault_addr: "https://{{ inventory_hostname }}.node.{{ consul_dns_domain }}:{{ vault_default_port }}``

.. data:: vault_init_json

   Initial JSON configuration for Vault

   default: ``{"secret_shares": 4, "secret_threshold": 3}``

.. data:: vault_otp

   Whether or not to install
   `vault-ssh-helper <https://github.com/hashicorp/vault-ssh-helper/>`_ and
   configure Vault logins using
   `One Time Passwords <https://www.vaultproject.io/docs/secrets/ssh/>`_.

   default: ``true``

.. data:: ssh_helper_config

   Where to store the configuration file for the vault-ssh-helper.

   default: ``/etc/vault/ssh-helper.hcl``

.. data:: ssh_helper_version

   Which version of vault-ssh-helper to install

   default: ``0.1.0``

.. data:: ssh_helper_url

   Where to download the vault-ssh-helper binary file from

.. data:: ssh_helper_checksum

   Checksum of the archive containing the vault-ssh-helper binary
