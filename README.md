# Ansible Role: Giflossy

[![Build Status](https://travis-ci.org/maztch/ansible-role-giflossy.svg?branch=master)](https://travis-ci.org/maztch/ansible-role-giflossy)

Installs Giflossy from source, the fork of Gifsicle, on RedHat/CentOS and Debian/Ubuntu servers.

## Requirements

If you are using SSL/TLS, you will need to provide your own certificate and key files. You can generate a self-signed certificate with a command like `openssl req -x509 -nodes -days 365 -newkey rsa:2048 -keyout example.key -out example.crt`.


## Role Variables

Available variables are listed below, along with default values (see `defaults/main.yml`):

    giflossy_version: 1.91
    

Giflossy version to install.

    giflossy_options:
      - --disable-gifview
      - --disable-gifdiff

A list of extra options for build giflossy.


## Dependencies

None.

## Example Playbook

    - hosts: webservers
      vars_files:
        - vars/main.yml
      roles:
        - { role: maztch.giflossy }

*Inside `vars/main.yml`*:

    giflossy_options:
      - --disable-gifview

## License

MIT / BSD

