# Ouch snap

Snap packaging for [Ouch](https://github.com/ouch-org/ouch), painless compression and decompression in the terminal.

Unofficial build, not affiliated with or endorsed by the Ouch project.

## Build

```bash
snapcraft pack
```

## Install and try

```bash
sudo snap install ./ouch_0.8.3_*.snap --dangerous
sudo snap connect ouch:removable-media   # optional: /media, /mnt
ouch compress ./my-dir ./my-dir.tar.zst
ouch decompress ./my-dir.tar.zst --dir ./restored
```

## Update to a new upstream release

Change `version` and `source-tag` in `snap/snapcraft.yaml`, then rebuild.

## License

The packaging is MIT-licensed (see `LICENSE`). Ouch is MIT-licensed; its dependencies carry their own licenses.
