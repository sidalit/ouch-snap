# Ouch snap

[![ouch](https://snapcraft.io/ouch/badge.svg)](https://snapcraft.io/ouch)

Snap packaging for [Ouch](https://github.com/ouch-org/ouch), painless compression and decompression in the terminal.

Unofficial build, not affiliated with or endorsed by the Ouch project.

## Build

```bash
snapcraft pack
```

## Install and try

<a href="https://snapcraft.io/ouch"><img alt="Get it from the Snap Store" src="https://snapcraft.io/en/dark/install.svg" width="180"></a>

```bash
sudo snap install ouch                   # or a local build: ./ouch_0.8.3_*.snap --dangerous
sudo snap connect ouch:removable-media   # optional: /media, /mnt
ouch compress ./my-dir ./my-dir.tar.zst
ouch decompress ./my-dir.tar.zst --dir ./restored
```

## Update to a new upstream release

Change `source-tag` in `snap/snapcraft.yaml`, then rebuild.

## Automation

Builds, publishing, and dependency updates use [snap-automation](https://github.com/sidalit/snap-automation).

## License

The packaging is MIT-licensed (see `LICENSE`). Ouch is MIT-licensed; its dependencies carry their own licenses.
