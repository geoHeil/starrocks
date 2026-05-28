# StarRocks Nix shell

Use this when you want the same build tools on Linux and Apple Silicon macOS.

```bash
nix develop
starrocks-build-env --print
```

Build StarRocks from the repository root:

```bash
starrocks-build-env --fe
starrocks-build-env --be
```

The wrapper only sets up tools and environment variables. It still uses the
normal StarRocks build scripts and third-party dependency flow.

CI runs `nix flake check` on:

- `x86_64-linux`
- `aarch64-linux`
- `aarch64-darwin`
