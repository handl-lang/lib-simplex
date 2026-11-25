# lib-simplex

Simplex noise generators — Handl stdlib port. Ships both the `.hnl`
sources under `src/` and a const-only Rust crate (`src/lib.rs`) that
re-exports them.

## Layout

| path | role |
| --- | --- |
| `src/simplex.hnl` | the .hnl sources |
| `src/simplex.test.hnl` | the .hnl test suite |
| `src/lib.rs` | const-only crate re-exporting the source |
| `pkg.hnl`, `scripts/hnl-gate.sh`, `workflows/gate.yaml` | manifest / gate / bupha entry |

## Contract

- Pure `.hnl` simplex noise; `src/lib.rs` only re-exports the source
  as consts for Rust consumers. Sibling of `lib-perlin`.

## Verification

```bash
HNL=../host-cli/target/debug/hnl scripts/hnl-gate.sh
./ci.sh                # full gate (bupha entry)
```

## License

MIT.

<!-- myco:agent-awareness -->

## Agent awareness

- Session start / any work discussion: run `myco status --prompt`
  before proposing next steps — know the board first.
- User describes new work → offer to capture it (`myco todo add`,
  `issue new`, `proposal new`). Don't wait to be asked.
- Picking up a task: `myco resume <ID>` is the briefing.
- Wrapping up: `myco handoff <ID>` anything resumable; keep statuses
  honest (claimed → in-progress → blocked/done).

<!-- /myco:agent-awareness -->
