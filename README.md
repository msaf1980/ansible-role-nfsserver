# Ansible role `nfsserver`

An Ansible role for setting up a NFS server.

- Install necessary packages
- Export filesystem
- Export filesystem for PXE boot

## Requirements

No specific requirements

## Role Variables

*TODO*

| Variable              | Default                        | Comment                                                          |
| :---                  | :---                           | :---                                                             |
| `pxeserver_images`    | []                             | List of filesystems for PXEboot images to be exported            |
| `nfsserver_exports`   | []                             | List of filesystems for be exported                              |

You can specify the boot images to be served with the variable `pxeserver_images`, a dict containing the keys listed below. Keys are *mandatory* unless specified.

| Key              | Value                                                             |
| :---             | :---                                                              |
| `name`           | Name                                                              |

## Dependencies

This role has no dependsies.

## Example Playbook

See the [test playbook](tests/test.yml)

## Testing

The `tests` directory contains tests for this role in the form of a Vagrant environment. You should install the dependent roles

```ShellSession
$ cd tests/
$ vagrant up
```

The last command creates a new CentOS 7 VM and applies the playbook [`test.yml`](tests/test.yml). This should result in a working PXE server.

## Contributing

Issues, feature requests, ideas are appreciated and can be posted in the Issues section. Pull requests are also very welcome. Preferably, create a topic branch and when submitting, squash your commits into one (with a descriptive message).

## License

BSD

## Further reading

## Author Information

Michail Safronov (msaf1980@gmail.com)
