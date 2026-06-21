# Changelog

## [v0.73.1] - 2026-06-19

### Changed
- Updated to NetBird v0.73.1

### Upstream Release Notes
## Release Notes for v0.73.1

### What's New

#### Client Improvements
- Fixed profile regressions affecting **`up --profile`** and **`status`** commands.  
  https://github.com/netbirdio/netbird/pull/6479
- Reduced **false-positive DNS health warnings**.  
  https://github.com/netbirdio/netbird/pull/6453
- Fixed **DNS custom zone teardown issues**, including handler leaks and external CNAME resolution.  
  https://github.com/netbirdio/netbird/pull/6445

#### Management Improvements
- Removed **database calls from nested loops** to improve efficiency.  
  https://github.com/netbirdio/netbird/pull/6470
- Fetched **complete user data in ValidateTunnelPeer**.  
  https://github.com/netbirdio/netbird/pull/6457
- Reduced **sync and login transaction overhead**.  
  https://github.com/netbirdio/netbird/pull/6472
- Added **peer metadata diff logging**.  
  https://github.com/netbirdio/netbird/pull/6468

#### Infrastructure & Tooling
- Removed the **`v` prefix from Docker image tags**.  
  https://github.com/netbirdio/netbird/pull/6471
- Improved **FreeBSD port scripts** to correctly handle release candidates when fetching tags.  
  https://github.com/netbirdio/netbird/pull/6480

### New Contributors
- @bison made their first contribution in https://github.com/netbirdio/netbird/pull/6457

**Full Changelog**: https://github.com/netbirdio/netbird/compare/v0.73.0...v0.73.1
