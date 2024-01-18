# Webarchitects cv Ansible role

[![pipeline status](https://git.coop/webarch/cv/badges/master/pipeline.svg)](https://git.coop/webarch/cv/-/commits/master)

This repository contains an Ansible role to install and update [cv, the CiviCRM command line interface](https://github.com/civicrm/cv).

## Role Variables

There are eight [default variables](defaults/main.yml), set `cv` to `true` for the tasks in this role to be run, it defaults to `false`, the other variables should only need changing if this role isn't run as `root` and you wish to install cv into a users `~/hom/bin`, `cv_bin`, `cv_bash_completion_dir` and `cv_download_dir` directories need to be writable by the `cv_owner`:

| Variable name            | Default value               | Comment                                        |
|--------------------------|-----------------------------|------------------------------------------------|
| `cv`                     | `true`                      | Run the tasks in this role.                    |
| `cv_bash_completion_dir` | `/etc/bash_completion.d`    | Bash_completion directory.                     |
| `cv_bin`                 | `/usr/local/bin`            | The directory into which cv will be installed. |
| `cv_download_dir`        | `/root`                     | The directory used for downloading files.      |
| `cv_group`               | `"{{ cv_owner }}"`          | The group for the cv files.                    |
| `cv_owner`               | `root`                      | The owner of the cv files.                     |
| `cv_pkgs_present`        | `bash-completion` `php-cli` | Required packages.                             |
| `cv_verify`              | `true`                      | Verify the variables that start with `cv_`     |

See also the [meta/argument_specs.yml](meta/argument_specs.yml) for all the variables this role uses, including the internal ones.

## Repository

The primary URL of this repo is [`https://git.coop/webarch/cv`](https://git.coop/webarch/cv) however it is also [mirrored to GitHub](https://github.com/webarch-coop/ansible-role-cv) and [available via Ansible Galaxy](https://galaxy.ansible.com/chriscroome/cv).

See the [GitLab releases page](https://git.coop/webarch/cv/-/releases) for details regarding each version, *please use a specific version* since the master branch is used for development.

This role can also be used with the [localhost repo](https://git.coop/webarch/localhost) to install cv locally.

## Copyright

Copyright 2021-2024 Chris Croome, &lt;[chris@webarchitects.co.uk](mailto:chris@webarchitects.co.uk)&gt;.

This role is released under [the same terms as Ansible itself](https://github.com/ansible/ansible/blob/devel/COPYING), the [GNU GPLv3](LICENSE).
