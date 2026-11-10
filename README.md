# JackGraph (RenkuOS)

> This repository is the source of the `jackgraph` package for RenkuOS. Built
> packages are on its [Releases](https://github.com/rations/jack-graph-renku/releases) page, and
> [renku-audio](https://github.com/rations/renku-audio) lists the whole audio stack.

A native RenkuOS application (Interface Kit) that acts as a **JACK patchbay and server
control**: start and stop the JACK server, adjust its settings, and view and manage port
connections on a graph canvas. It is the GUI front-end of the Kasen audio stack — see
[renku-audio](https://github.com/rations/renku-audio) for how the pieces fit together.

## Requirements

- The **`jack`** package (jack-port-renku): `libjack` plus a `jackd` it can start/stop and
  connect to.

## Build / install

Native on RenkuOS (x86_64):

- **Prebuilt package:** `packaging/make-hpkg.sh` → `jackgraph-0.2-2-x86_64.hpkg`, then
  `pkgman install ./jackgraph-*.hpkg`.
- **From source:** `./build-from-source.sh` (build jack-port-renku from source first — the
  Makefile links `-ljack` from the non-packaged tree).

## License

MIT — see [LICENSE](LICENSE).
