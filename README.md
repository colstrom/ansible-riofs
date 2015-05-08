# ansible-riofs

[riofs](https://github.com/skoobe/riofs) - RioFS is an userspace filesystem for Amazon S3 buckets for servers.

[![Platforms](http://img.shields.io/badge/platforms-ubuntu-lightgrey.svg?style=flat)](#)

Tunables
--------
* `riofs_mountpoint` (string) - Where to mount the bucket?
* `riofs_build_path` (string) - Path to use when compiling RioFS
* `riofs_clean_after_build` (boolean) - Clean working directory after compilation?
* `riofs_always_reinstall` (boolean) - Reinstall RioFS if it is already present?
* `riofs_user` (string) - User to run riofs as
* `riofs_group` (string) - Group to run riofs as
* `riofs_users` (list) - Other users that should have access to the bucket
* `riofs_bucket_name` (string) - Name of the bucket to mount

Dependencies
------------
* [colstrom.upstart](https://github.com/colstrom/ansible-upstart/)

Example Playbook
----------------
    - hosts: servers
      roles:
         - role: colstrom.riofs
           riofs_mountpoint: /mnt/s3
           riofs_bucket_name: mybucketname

License
-------
[MIT](https://tldrlegal.com/license/mit-license)

Contributors
------------
* [Chris Olstrom](https://colstrom.github.io/) | [e-mail](mailto:chris@olstrom.com) | [Twitter](https://twitter.com/ChrisOlstrom)
* Justin Scott
* Steven Harradine
