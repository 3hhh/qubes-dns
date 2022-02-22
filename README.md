# qubes-dns

Some helper scripts to setup a dedicated DNS VM in [Qubes OS](https://www.qubes-os.org/). All of them can be used individually.

`dns_client`: Can be used to forward all DNS requests from upstream VMs to a dedicated VM or to a locally running DNS server. See its help text for further details.

`dns_server`: Starts an `unbound` DNS server (you still need to supply the config) and sets up the Qubes OS firewall accordingly. Intended to be used inside a dedicated DNS server VM, e.g. from `/rw/config/rc.local`.

`dns_pin2hosts`: Updates `/etc/hosts` based on the hostnames resolved by the locally running Qubes OS firewall. Intended to be run inside firewall VMs in combination with `systemd-resolved` or `dnsmasq` to pin/indefinitely cache those hostnames for upstream VMs. This should ensure that the Qubes OS firewall hostnames are always in sync to DNS requests from upstream VMs. Usually run from `/rw/config/qubes-firewall-user-script`.

Use what you need for your purpose and at your own risk!

The scripts currently require [blib](https://github.com/3hhh/blib) to be [installed](https://github.com/3hhh/blib#installation) in the template.

## Copyright

© 2022 David Hobach
GPLv3

See `LICENSE` for details.
