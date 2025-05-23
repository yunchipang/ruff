## Getting started

1. [Install `uv`](https://docs.astral.sh/uv/getting-started/installation/)

- Unix: `curl -LsSf https://astral.sh/uv/install.sh | sh`
- Windows: `powershell -c "irm https://astral.sh/uv/install.ps1 | iex"`

1. Build ty: `cargo build --bin ty --release`
1. `cd` into the benchmark directory: `cd scripts/ty_benchmark`
1. Run benchmarks: `uv run benchmark`

## Known limitations

ty only implements a tiny fraction of Mypy's and Pyright's functionality,
so the benchmarks aren't in any way a fair comparison today. However,
they'll become more meaningful as we build out more type checking features in ty.

### Windows support

The script should work on Windows, but we haven't tested it yet.
We do make use of `shlex` which has known limitations when using non-POSIX shells.
