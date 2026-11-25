# Changelog

All notable changes to this action are documented in this file.

## 2.0.0

### Breaking changes

- The action was renamed from `yukiakai212/publish-tag` to `yukiakai212/resolve-release-metadata`. Published `publish-tag` releases remain available, but new workflows must use the new action reference.
- The action no longer reads a GitHub tag implicitly. Provide `raw-version`, or select a supported package manifest with `package-type` and `package-directory`.
- `prefix` was renamed to `prefix-to-remove`. It is now optional and has no default value.
- The former `tag` output, which represented an npm publish tag, was removed. Use `release-tag` for a Git release tag; it is always `v` followed by `version` and never includes build metadata.

### Added

- Resolve version text directly through `raw-version`.
- Resolve version text from Node.js (`package.json`) and Cargo (`Cargo.toml`) package manifests.
