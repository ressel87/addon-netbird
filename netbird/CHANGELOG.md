# Changelog

## [0.78.1.1] - 2026-09-10

Fork-only release (same NetBird v0.78.1 binary). Version scheme is
`<netbird-version>.<fork-release>`; Renovate replaces it with the next NetBird release.

### Changed
- Renamed add-on and repository to "BornData fork"; maintainer BornData.dk <support@borndata.dk>
- Synced with upstream netbirdio/addon-netbird:
  - Self-heal a stale `app.netbird.io` Management URL on startup (upstream #401)
  - Optional config fields (`admin_url`, `management_url`, `setup_key`) and FQDN-capable hostname validation
  - CI hardening in GitHub workflows

## [v0.78.1] - 2026-09-04

### Changed
- Updated to NetBird v0.78.1

### Upstream Release Notes
## What's Changed
* [management] Serve networks with peer-based routers from the SQLite network map by @mlsmaycon in https://github.com/netbirdio/netbird/pull/7424


**Full Changelog**: https://github.com/netbirdio/netbird/compare/v0.78.0...v0.78.1
