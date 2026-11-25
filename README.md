# lib-simplex

Simplex noise generators — Handl stdlib port.

Ships both the .hnl sources under `src/` and a const-only Rust crate
(`src/lib.rs`) that re-exports them.

## Layout

```text
src/simplex.hnl       the .hnl sources
src/simplex.test.hnl  the .hnl test suite
src/lib.rs            const-only crate re-exporting the source
pkg.hnl               package manifest — modules, deps, description, license
workflows/gate.yaml                 bupha entry (handl-gates) → scripts/hnl-gate.sh
```

## Gate

```bash
HNL=../host-cli/target/debug/hnl scripts/hnl-gate.sh
HNL=../host-cli/target/debug/hnl scripts/hnl-gate.sh  # full gate (bupha entry)
```

## Development

```bash
cargo xtask gate        # fmt --check → clippy -D warnings → test → doc
```

`cargo xtask` wraps the repo's `xtask/` crate (`fmt`, `clippy`, `test`, `doc`,
`check`, `gate`).

## License

MIT.
