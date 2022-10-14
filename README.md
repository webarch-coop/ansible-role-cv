# cv

[![pipeline status](https://git.coop/webarch/cv/badges/master/pipeline.svg)](https://git.coop/webarch/cv/-/commits/master)

An Ansible role to install and update [cv, the CiviCRM command line interface](https://github.com/civicrm/cv).

There are five [default variables](defaults/main.yml), these should only need changing if this role isn't run as `root` and you wish to install cv into a users `~/hom/bin`, `cv_bin` and `cv_download_dir` directories need to be writable by the `cv_owner`:

| Variable name            | Default value            | Comment                                        |
|--------------------------|--------------------------|------------------------------------------------|
| `cv`                     | `true`                   | Run the tasks in this role.                    |
| `cv_bin`                 | `/usr/local/bin`         | The directory into which cv will be installed. |
| `cv_download_dir`        | `/root`                  | The directory used for downloading files.      |
| `cv_owner`               | `root`                   | The owner of the cv files.                     |
| `cv_group`               | `"{{ cv_owner }}"`       | The group for the cv files.                    |


The primary URL of this repo is [`https://git.coop/webarch/cv`](https://git.coop/webarch/cv) however it is also [mirrored to GitHub](https://github.com/webarch-coop/ansible-role-cv) and [available via Ansible Galaxy](https://galaxy.ansible.com/chriscroome/cv).

See the [GitLab releases page](https://git.coop/webarch/cv/-/releases) for details regarding each version, *please use a specific version* since the master branch is used for development.

This role can also be used with the [localhost repo](https://git.coop/webarch/localhost) to install cv locally.

