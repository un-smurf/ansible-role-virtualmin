# Ansible Role: virtualmin
 
[![ansible-lint](https://github.com/un-smurf/ansible-role-virtualmin/actions/workflows/ansible-lint.yml/badge.svg)](https://github.com/un-smurf/ansible-role-net-tools/actions/workflows/ansible-lint.yml)
![GitHub release (latest by date)](https://img.shields.io/github/v/tag/un-smurf/ansible-role-virtualmin?color=yellow)
[![License: MIT](https://img.shields.io/badge/License-MIT-blueviolet.svg)](https://opensource.org/licenses/MIT)

Install Virtiualmin GPL - https://www.virtualmin.com/download/

## Requirements

Needs to be a new blank server.
A FQDN needs to be set. This is required by Virtualmin.

## Dependencies

None but see Requirements

## Install

	ansible-galaxy role install git+https://github.com/un-smurf/ansible-role-virtualmin,main,un-smurf.virtualmin

## Role Variables

Available variables are listed below, along with default values (see `defaults/main.yml`):

	virtualmin_bin_location: /sbin/virtualmin

used to check if virtualmin is installed

	virtualmin_download_url: http://software.virtualmin.com/gpl/scripts/install.sh

Download URL

	virtualmin_download_dest: /tmp/install.sh

Download Location

	virtualmin_fqdn: "server1.example.com"

FQDN as required by virtualmin

	virtualmin_bundle: LAMP

Bundle Type (LAMP or LEMP)


## Example Playbook

    - hosts: servers
	
	vars_files:
    - vars/main.yml
	
      roles:
        - un-smurf.virtualmin


Inside `vars/main.yml`:


	virtualmin_bundle: LAMP
	virtualmin_fqdn: "server1.example.com"
	

## License

MIT

## Author Information

This role was created in 2024 by un-smurf.
