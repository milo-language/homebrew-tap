# Milo Homebrew tap

Homebrew formula for [Milo](https://github.com/milo-language/milo) — a memory-safe
systems language that compiles to LLVM IR.

```sh
brew install milo-language/tap/milo
milo --version
```

Works on macOS (Apple Silicon and Intel) and Linuxbrew (x86_64 and arm64).

Milo links what it compiles with clang. macOS ships one with the Xcode Command Line
Tools (`xcode-select --install`); on Linux install your distribution's clang, or
`brew install llvm`.

## For maintainers

`Formula/milo.rb` is **generated** — do not edit it by hand. The release workflow in
the main repo renders it from the published tarballs (hashing the actual bytes, so the
`sha256` can never drift from what the release serves) and pushes the result here on
every `v*` tag.

Source of truth: [`scripts/render-formula.ts`](https://github.com/milo-language/milo/blob/main/scripts/render-formula.ts)
