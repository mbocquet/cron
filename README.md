# cron

Ansible role to handle cron's maintenance window.

## Requirements

None.

## Role Variables

* main crontab file
  cron_main_crontab: '/etc/crontab'
* default maintenance window start hour (24h format)
  cron_hour_start: 4
* default maintenance window in hours (24h format)
  cron_hour_duration: 2

With these parameters, cron minutes and hours in **/etc/crontab** will be randomized to fit in the maintenance window starting from 04:00 with a duration of 02:00. So from 04:00 to 06:00.

## Dependencies

None.

## Install this role as submodule in a git repository

`git submodule add https://github.com/mbocquet/cron.git roles/cron`

## Example Playbook

    - hosts: servers
      roles:
         - { role: cron, cron_hour_start: 4 }

## License

GPLv3

## Author Information

http://www.sekoya.org
