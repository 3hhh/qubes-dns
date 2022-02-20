# qubes-dns

Some helper scripts to setup a dedicated DNS VM in [Qubes OS](https://www.qubes-os.org/).

`dns_client` can be used to forward all DNS requests from upstream VMs to a dedicated VM, `dns_server` setups an `unbound` DNS server (you still need to supply the config).

Use what you need and at your own risk!

The scripts currently require [blib](https://github.com/3hhh/blib) to be [installed](https://github.com/3hhh/blib#installation) in the template.

## Copyright

© 2022 David Hobach
GPLv3

See `LICENSE` for details.
