Ansible Role SVN - Server
=========================

Installs [Apache SVN](https://subversion.apache.org/) (Subversion) on any RHEL/CentOS or Debian/Ubuntu Linux system.

## Requirements

The `svnserve` service, which allows access to repositories via the `svn://` protocol runs on port 3690 by default, so please make sure that port is open on your firewall.

## Role Variables

Available variables are listed below, along with default values (see `defaults/main.yml`):

    svn_repository_home: /var/svn

The SVN repository directory that will be served by `svnserve` through Apache.

    svn_create_test_repo: true

Whether to create a example respository 'testrepo', which will be available at `http://[hostname]/svn/testrepo`.

## Example Playbook

    - hosts: servers
      roles:
        - raben2.ansible-role-svn

## License

MIT / BSD

## Author Information

Georg Rabenstein raben2