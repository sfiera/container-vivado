Vivado in a Container
=====================

Setup
-----

Install and start Docker or Colima (with Intel support).

Download the Vivado 2023.2 installer and run `setup`:

```
$ INSTALLER=FPGAs_AdaptiveSoCs_Unified_2023.2_1013_2256_Lin64.bin
$ shasum $INSTALLER
ea98fc804c6fb074c1ea8c672d2bda728f79e6fa  FPGAs_AdaptiveSoCs_Unified_2023.2_1013_2256_Lin64.bin
$ mkdir -p ~/.local/bin
$ ./container-vivado setup $INSTALLER
```

Ensure `~/.local/bin` is in your `$PATH`.

Usage
-----

Call `vivado` within a Git repository. The repository will be mapped into a Docker container and Vivado will run inside that container.

Notes
-----

Currently only supports Vivado 2023.2, the version used by [Game Bub](https://github.com/elipsitz/gamebub).

Credits
-------

Derived largely from [yokeTH/vivado-mac](https://github.com/yokeTH/vivado-mac)
