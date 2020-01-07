Saltstack for arm64 Gentoo Overlay
==================================

This overlay adds the ~arm64 keyword to app-admin/salt/salt-2019.2.2 and
dev-python/libnacl-1.6.1 ebuilds.  Your repos.conf file/directory will need
the following added:

```
[saltstack-arm64-overlay]
location = /var/db/repos/saltstack-arm64-overlay
sync-type = git
sync-uri = https://github.com/epoelke/saltstack-arm64-overlay.git
```

The package keywords will need to be updated as well since salt and several
of its dependencies are not marked as stable.

Example:
```
=app-admin/salt-2019.2.2::saltstack-arm64-overlay ~arm64
=dev-python/libnacl-1.6.1::saltstack-arm64-overlay ~arm64

# deps
=dev-python/msgpack-0.6.1 ~arm64
=www-servers/tornado-4.5.3 ~arm64
=dev-python/pyzmq-17.1.0 ~arm64
=dev-python/pycryptodome-3.6.6 ~arm64
```
