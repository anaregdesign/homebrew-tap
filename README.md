# Lantern Homebrew Tap

Homebrew tap for [Lantern](https://github.com/anaregdesign/lantern) — an in-memory
graph key-vertex-store ("key-vertex-store") served over Connect/HTTP-2.

> [!NOTE]
> The cask files under `Casks/` are generated and pushed automatically by
> [GoReleaser](https://goreleaser.com) on each Lantern release. **Do not edit them by
> hand.**

## Install

```sh
brew tap anaregdesign/tap
brew install --cask lantern        # the Lantern server (binary: lantern)
brew install --cask lantern-cli    # the Lantern CLI (binary: lantern-cli)
```

Upgrade later with:

```sh
brew update && brew upgrade --cask lantern lantern-cli
```

## Notes

- The binaries are not Apple-notarized, so each cask clears the macOS quarantine bit
  on install via a `postflight` `xattr` call.
- These casks track the root Lantern release (`vX.Y.Z`). The container images
  (`ghcr.io/anaregdesign/lantern`, `…/lantern-mcp`, `…/lantern-admin`) and the MCP and
  admin components are published separately — see the
  [main repository](https://github.com/anaregdesign/lantern).

## License

Apache-2.0, matching the upstream project.
