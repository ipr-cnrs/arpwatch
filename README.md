# arpwatch

1. [Overview](#overview)
2. [Role Variables](#role-variables)
3. [Example Playbook](#example-playbook)
4. [Configuration](#configuration)
5. [Development](#development)
6. [License](#license)
7. [Author Information](#author-information)

## Overview

Manage Arpwatch installation and configuration.

## Role Variables

* **arpwatch__base_packages** : List of base packages in order to provide `arpwatch` [default : `arpwatch`].
* **arpwatch__enabled** : Enable or disable support for Arpwatch on a given host [default : `True`].
* **arpwatch__service_manage** : If the arpwatch service should be managed [default : `True`].
* **arpwatch__service_name** : The service name to manage [default : `arpwatch`].
* **arpwatch__conf_src** : Template used to provide configuration file [default : `../templates/etc/arpwatch.conf.j2`].
* **arpwatch__conf_username** : Username that should run Arpwatch [default : `arpwatch`].
* **arpwatch__conf_args** : Arguments to apply to Arpwatch [default : `-N -p`].

## Example Playbook

* Use defaults vars :

``` yml
- hosts: serverXYZ
  roles:
    - role: ipr-cnrs.arpwatch
```

## Configuration

This role will :
* Install needed packages to provide `arpwatch` service.
* Manage `arpwatch` configuration (/etc/arpwatch.conf).
* Allow to set the user that run Arpwatch.
* Allow to set arguments to pass Arpwatch service.
* Ensure `arpwatch` service is enabled and started.
* Ensure to restart `arpwatch` service if configuration changed.

## Development

This source code comes from our [Gogs instance][arpwatch source] and the [Github repo][arpwatch github] exist just to be able to send the role to Ansible Galaxy…

But feel free to send issue/PR here :)

Thanks to this [hook][gogs to github hook], Github automatically got updates from our [Gogs instance][arpwatch source] :)

## License

[WTFPL][wtfpl website]

## Author Information

Jérémy Gardais
* Source : [on IPR's Gogs][arpwatch source]
* [IPR][ipr website] (Institut de Physique de Rennes)

[gogs to github hook]: https://stackoverflow.com/a/21998477
[arpwatch source]: https://git.ipr.univ-rennes1.fr/cellinfo/ansible.arpwatch
[arpwatch github]: https://github.com/ipr-cnrs/arpwatch
[wtfpl website]: http://www.wtfpl.net/about/
[ipr website]: https://ipr.univ-rennes1.fr/
