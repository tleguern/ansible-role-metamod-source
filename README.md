# Ansible Role: metamode-source

[![builds.sr.ht status](https://builds.sr.ht/~tleguern/ansible-role-metamod-source.svg)](https://builds.sr.ht/~tleguern/ansible-role-metamod-source?)

An Ansible role that installs and configures [Metamod:Source](http://www.metamodsource.net/).

Automatic testing is provided using molecule's delegated driver and <https://builds.sr.ht>.

## Requirements

An ansible role dedicated to the installation of SteamCMD such as [ansible-steamcmd](https://github.com/tleguern/ansible-steamcmd) or any role providing the `{{ steamcmd_user }}` variable.

## Role Variables

| Variable | Description | Default |
|----------|-------------|---------|
| `steamcmd_user` | User name for steamcmd | `steam` |
| `metamod_source_url` | URL pointing to metamod releases | `https://mms.alliedmods.net/mmsdrop` |
| `metamod_source_branch` | Release branch | `1.11` |
| `metamod_source_install_path` | Installation directory | mandatory |

## Dependencies

None

## Example Playbook

```yaml
- hosts: game
  vars:
    metamod_source_install_path: /home/steam/cstrike-source/cstrike
  roles:
    - role: ansible-steamcmd
    - role: ansible-role-cstrike-source
    - role: ansible-role-metamod-source
```

## License

ISC

## Contributing

Either send [send GitHub pull requests](https://github.com/tleguern/ansible-role-metamod-source) or [send patches on SourceHut](https://lists.sr.ht/~tleguern/misc).

## Author Information

Tristan Le Guern <tleguern@bouledef.eu>
