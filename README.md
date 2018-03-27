# Ansible Role: Giflossy

Installs Giflossy from source, the fork of Gifsicle, on RedHat/CentOS and Debian/Ubuntu servers.

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

