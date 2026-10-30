# JackGraph (RenkuOS)

> This repository is the source of the `jackgraph` package, part of the
> [JackDAW stack](https://github.com/rations/jackDAW-renku) for RenkuOS. The 0.5
> release's `install.sh` is for Haiku hrev60256; there is no RenkuOS release yet.

A native RenkuOS application (Interface Kit) that acts as a **JACK patchbay and server
control**: start and stop the JACK server, adjust its settings, and view and manage port
connections on a graph canvas. It is the GUI front-end of the JackDAW audio stack — see
[jackDAW-renku/STACK.md](https://github.com/rations/jackDAW-renku/blob/master/STACK.md) for how the pieces fit together.

## Requirements

- The **`jack`** package (jack-port-renku): `libjack` plus a `jackd` it can start/stop and
  connect to.

## Build / install

Native on RenkuOS (x86_64):

- **Prebuilt package:** `packaging/make-hpkg.sh` → `jackgraph-0.1-1-x86_64.hpkg`, then
  `pkgman install ./jackgraph-*.hpkg`.
- **From source:** `./build-from-source.sh` (build jack-port-renku from source first — the
  Makefile links `-ljack` from the non-packaged tree).

A HaikuPorts recipe is in `packaging/jackgraph-0.1.recipe` (validate with
`haikuporter -c jackgraph`).

## License

MIT — see [LICENSE](LICENSE).
