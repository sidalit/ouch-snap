<div align="center">

<img src="snap/gui/ouch.png" alt="Ouch logo" width="128" />

# Ouch

**Painless compression and decompression**

[![ouch](https://snapcraft.io/ouch/badge.svg)](https://snapcraft.io/ouch)
[![Base: core26](https://img.shields.io/badge/Base-core26-2C8C3C?logo=canonical&logoColor=white)](https://snapcraft.io/core26)
![Confinement: strict](https://img.shields.io/badge/Confinement-strict-2C8C3C)
[![Maintainer: sidaliteir](https://img.shields.io/badge/Maintainer-sidaliteir-2C8C3C?logo=snapcraft&logoColor=white)](https://snapcraft.io/publisher/sidaliteir)
![Architectures: amd64 and arm64](https://img.shields.io/badge/Architectures-amd64%20%7C%20arm64-2C8C3C?logo=linux&logoColor=white)

[Getting Started](#getting-started) · [Configure](#configure) · [Limitations](#limitations) · [Build](#build) · [Support](#support) · [License](#license)

Unofficial snap packaging for [Ouch](https://github.com/ouch-org/ouch), a command-line tool for creating and extracting archives.

</div>

---

## Getting Started

<a href="https://snapcraft.io/ouch"><img alt="Get it from the Snap Store" src="https://snapcraft.io/en/dark/install.svg" width="180"></a>

```bash
sudo snap install ouch
ouch compress ./my-dir ./my-dir.tar.zst
ouch decompress ./my-dir.tar.zst --dir ./restored
```

Ouch selects the compression format from the archive's file extension.

## Configure

There are no `snap set` options. Choose the archive name, input files and output directory on the command line. Use `ouch --help`, `ouch compress --help` or `ouch decompress --help` for available options.

To work with archives under `/media` or `/mnt`:

```bash
sudo snap connect ouch:removable-media
```

## Limitations

- Work in a normal folder under your home directory or connected removable storage.
- Hidden files directly under your normal home directory and arbitrary system paths are inaccessible under strict confinement.

## Build

```bash
git clone https://github.com/sidalit/ouch-snap.git
cd ouch-snap
sudo snap install snapcraft --classic
snapcraft pack
```

## Support

- **Installation or snap issues:** [open a packaging issue](https://github.com/sidalit/ouch-snap/issues).
- **Application bugs:** [report them upstream](https://github.com/ouch-org/ouch/issues).

## License

Snap packaging: [MIT](https://github.com/sidalit/ouch-snap/blob/main/LICENSE).
