# Hikari Linux Calamares configuration

First-boot account and desktop setup for Hikari Linux, using Calamares in OEM
setup mode. The approved Hikari Linux logo is kept as a vector SVG.

On Linux with GNU coreutils:

```sh
make install PREFIX=/usr DESTDIR="$pkgdir"
```

The setup requires Calamares, Xorg/startx, KWin X11, feh, xrandr, xdpyinfo,
systemd, and the desktop integration supplied by the image. Packaging must
replace/conflict with `asahi-calamares-configs`: both own the Calamares settings,
`first-time-setup.sh`, and `calamares.service`. Enable the service only in images
that are prepared for first-boot setup; it configures users on the running system.

The snapshot's `asahi,kblang-code` device-tree property and Apple keyboard
mappings are retained. Rebranding does not validate new hardware support.

## Origin and license

Based on the preserved [asahi-calamares-configs snapshot](https://github.com/HikariLinux/asahi-calamares-configs/tree/8c957638e732d5b3a33647e026317eec0b52f7a7),
commit `8c957638e732d5b3a33647e026317eec0b52f7a7`. Original history and snapshot tags are retained.
Hikari Linux maintains this project independently; this is not an official
Asahi Linux release. Original copyright and license notices are preserved.
Hikari Linux changes use the same [MIT license](LICENSE).

Calamares configuration files retain their CC0-1.0 notices. The Hikari Linux
logo is provided under the MIT license.
