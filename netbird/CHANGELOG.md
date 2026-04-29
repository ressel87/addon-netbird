# Changelog

## [v0.70.3] - 2026-04-29

### Changed
- Updated to NetBird v0.70.3

### Upstream Release Notes
## What's Changed
* [client] Enable UI autostart for silent and MSI installs by @shuuri-labs in https://github.com/netbirdio/netbird/pull/6026
* [management] Prevent JWT reuse during peer login by @bcmmbaga in https://github.com/netbirdio/netbird/pull/6002
* [client] Use BindListener for all userspace bind in lazyconn activity by @lixmal in https://github.com/netbirdio/netbird/pull/6028
* [client] Tolerate EEXIST when adding macOS scoped default routes by @lixmal in https://github.com/netbirdio/netbird/pull/6027
* [client] Trigger mobile submodule bump PRs on release tags by @pappz in https://github.com/netbirdio/netbird/pull/6029


**Full Changelog**: https://github.com/netbirdio/netbird/compare/v0.70.2...v0.70.3

## [v0.70.2] - 2026-04-29

### Changed
- Updated to NetBird v0.70.2

### Upstream Release Notes
## What's Changed
* [client] Move macOS sleep detection into the daemon (purego) by @lixmal in https://github.com/netbirdio/netbird/pull/5926
* [client] Fix Windows installer upgrade detection for pre-0.70.1 installs by @lixmal in https://github.com/netbirdio/netbird/pull/6025
* [misc] Add comment automation on release workflow for PRs by @jnfrati in https://github.com/netbirdio/netbird/pull/6016


**Full Changelog**: https://github.com/netbirdio/netbird/compare/v0.70.1...v0.70.2

## [v0.70.1] - 2026-04-29

### Changed
- Updated to NetBird v0.70.1

### Upstream Release Notes
## What's Changed
* [management] removed legacy network map code by @crn4 in https://github.com/netbirdio/netbird/pull/5565
* [management] Add Microsoft AD FS support for embedded Dex identity providers by @bcmmbaga in https://github.com/netbirdio/netbird/pull/6008
* [management] Handle single-string JWT group claim from IdPs by @bcmmbaga in https://github.com/netbirdio/netbird/pull/6014
* [client] Don't mark management disconnected on transient job stream errors by @pappz in https://github.com/netbirdio/netbird/pull/6005
* [relay] evict foreign client cache on disconnect by @pappz in https://github.com/netbirdio/netbird/pull/6015
* [self-hosted] fix(getting-started): Infinite healthcheck loop with existing traefik by @WalidDevIO in https://github.com/netbirdio/netbird/pull/5871
* [management] Drop netmap calculation on peer read by @bcmmbaga in https://github.com/netbirdio/netbird/pull/6006
* [client] Use WinRT COM for Windows toasts by @lixmal in https://github.com/netbirdio/netbird/pull/6013

## New Contributors
* @WalidDevIO made their first contribution in https://github.com/netbirdio/netbird/pull/5871

**Full Changelog**: https://github.com/netbirdio/netbird/compare/v0.70.0...v0.70.1

## [v0.70.0] - 2026-04-27

### Changed
- Updated to NetBird v0.70.0

### Upstream Release Notes
## What's Changed
* [self-hosted] add reverse proxy retention fields to combined YAML by @braginini in https://github.com/netbirdio/netbird/pull/5930
* [management] replace mailru/easyjson with netbirdio/easyjson fork by @braginini in https://github.com/netbirdio/netbird/pull/5938
* [client] Supress ICE signaling by @pappz in https://github.com/netbirdio/netbird/pull/5820
* [client] Prefer systemd-resolved stub over file mode regardless of resolv.conf header by @lixmal in https://github.com/netbirdio/netbird/pull/5935
* [client] Trust wg interface in firewalld to bypass owner-flagged chains by @lixmal in https://github.com/netbirdio/netbird/pull/5928
* [management] check policy for changes before actual db update by @crn4 in https://github.com/netbirdio/netbird/pull/5405
* [client] allow UDP packet loss in TestICEBind_HandlesConcurrentMixedTraffic by @pappz in https://github.com/netbirdio/netbird/pull/5953
* [client] fix goroutine leak in TestReceive_ProtocolErrorStreamReconnect by @pappz in https://github.com/netbirdio/netbird/pull/5951
* [client] fix port collision in TestUpload by @pappz in https://github.com/netbirdio/netbird/pull/5950
* [management] Propagate context changes to upstream middleware by @bcmmbaga in https://github.com/netbirdio/netbird/pull/5956
* [self-hosted] Use cscli lapi status for CrowdSec readiness check in installer by @lixmal in https://github.com/netbirdio/netbird/pull/5949
* [client] Add TTL-based refresh to mgmt DNS cache via handler chain by @lixmal in https://github.com/netbirdio/netbird/pull/5945
* [client] increase gRPC health check timeout to 5s by @pappz in https://github.com/netbirdio/netbird/pull/5961
* [management] refactor: changeable pat rate limiting by @crn4 in https://github.com/netbirdio/netbird/pull/5946
* [management] exclude peers for expiration job that have already been marked expired by @pascal-fischer in https://github.com/netbirdio/netbird/pull/5970
* [proxy] set session cookie path to root by @alsruf36 in https://github.com/netbirdio/netbird/pull/5915
* [management] unify peer-update test timeout via constant by @pappz in https://github.com/netbirdio/netbird/pull/5952
* [misc] Update sign pipeline version by @mlsmaycon in https://github.com/netbirdio/netbird/pull/5981
* [misc] Update release pipeline version by @mlsmaycon in https://github.com/netbirdio/netbird/pull/5995

## New Contributors
* @alsruf36 made their first contribution in https://github.com/netbirdio/netbird/pull/5915

**Full Changelog**: https://github.com/netbirdio/netbird/compare/v0.69.0...v0.70.0

## [v0.69.0] - 2026-04-20

### Changed
- Updated to NetBird v0.69.0

### Upstream Release Notes
## Release Notes for v0.69.0

### What's New
**Reverse Proxy IP Reputation Integration** 
Now you can use CrowdSec to block malicious traffic based on IP reputation on your exposed service in the reverse proxy.

This feature requires self-hosted installations to add another container to their deployment. See instructions in the [reverse proxy migration documentation](https://docs.netbird.io/selfhosted/migration/enable-reverse-proxy#step-7-optional-enable-crowd-sec-ip-reputation).

> For Cloud users, support is coming soon.

Learn more about [here](https://docs.netbird.io/manage/reverse-proxy).


**macOS p2p connectivity improvements**
We've improved macOS p2p connectivity with a better routing exclusion mechanism to avoid loops. Now the client doesn't add /32 routes per remote candidate addresses avoiding limitations on accessing remote peer's local addresses via tunnel connections. Learn more about [this change](https://github.com/netbirdio/netbird/pull/5918).
> To use the old behavior run:
> 
> `sudo netbird service reconfigure --service-env "NB_USE_LEGACY_ROUTING=true"`

#### Client Improvements
- Added **PCP support**.  This change adds support for the PCP protocol to the client to improve the rate of P2P connectivity. 
  https://github.com/netbirdio/netbird/pull/5219
- Added **--disable-networks flag** to block network selection for users.  
  https://github.com/netbirdio/netbird/pull/5896
- Fixed **clearing service env vars with --service-env ""**.  
  https://github.com/netbirdio/netbird/pull/5893
- Guarded against **container DNAT bypass of ACL rules in iptables**.  
  https://github.com/netbirdio/netbird/pull/5697
- Populated **NetworkAddresses on iOS for posture checks**.  
  https://github.com/netbirdio/netbird/pull/5900
- Reconnected **conntrack netlink listener on error**.  
  https://github.com/netbirdio/netbird/pull/5885
- Replaced **exclusion routes with scoped default + IP_BOUND_IF on macOS**.  
  https://github.com/netbirdio/netbird/pull/5918
- Fixed **incorrect SSH client config combining Host and Match directives**.  
  https://github.com/netbirdio/netbird/pull/5903
- Fixed **WGIface.Close deadlock when DNS filter hook re-enters GetDevice**.  
  https://github.com/netbirdio/netbird/pull/5916

#### Management Improvements
- Enforced **peer or peer groups requirement for network routers**.  
  https://github.com/netbirdio/netbird/pull/5894
- Reused **single cache store across all management server consumers**.  
  https://github.com/netbirdio/netbird/pull/5889
- Fixed **lint error on Google Workspace integration**.  
  https://github.com/netbirdio/netbird/pull/5907

#### Proxy Enhancements
- Added **CrowdSec IP reputation integration for reverse proxy**.  
  https://github.com/netbirdio/netbird/pull/5722
- Added **direct redirect to SSO**.  
  https://github.com/netbirdio/netbird/pull/5874

#### Infrastructure Improvements
- Updated **sign pipeline version to v0.1.2**.  
  https://github.com/netbirdio/netbird/pull/5884
- Added **CrowdSec LAPI container to self-hosted setup script**.  
  https://github.com/netbirdio/netbird/pull/5880

### New Contributors
- @MichaelUray made their first contribution in https://github.com/netbirdio/netbird/pull/5900
- @jnfrati made their first contribution in https://github.com/netbirdio/netbird/pull/5907

**Full Changelog**: https://github.com/netbirdio/netbird/compare/v0.68.3...v0.69.0

## [v0.68.3] - 2026-04-14

### Changed
- Updated to NetBird v0.68.3

### Upstream Release Notes
## What's Changed
* [management] revert ctx dependency in get account with backpressure by @crn4 in https://github.com/netbirdio/netbird/pull/5878
* [management] add context cancel monitoring by @pascal-fischer in https://github.com/netbirdio/netbird/pull/5879
* [misc] Add CI check for proto version string changes by @lixmal in https://github.com/netbirdio/netbird/pull/5854


**Full Changelog**: https://github.com/netbirdio/netbird/compare/v0.68.2...v0.68.3

## [v0.68.2] - 2026-04-13

### Changed
- Updated to NetBird v0.68.2

### Upstream Release Notes
## What's Changed
* [management] network map tests by @mlsmaycon in https://github.com/netbirdio/netbird/pull/5795
* [management] use sql null vars by @pascal-fischer in https://github.com/netbirdio/netbird/pull/5844
* [client] Use native firewall for peer ACLs in userspace WireGuard mode by @lixmal in https://github.com/netbirdio/netbird/pull/5668
* [misc] update dashboards by @pascal-fischer in https://github.com/netbirdio/netbird/pull/5840
* [management] update account delete with proper proxy domain and service cleanup by @pascal-fischer in https://github.com/netbirdio/netbird/pull/5817
* [management] allow local routing peer resource by @pascal-fischer in https://github.com/netbirdio/netbird/pull/5814
* [management] Revert "[management] allow local routing peer resource (#5814)" by @pascal-fischer in https://github.com/netbirdio/netbird/pull/5847
* [management] enable access log cleanup by default by @pascal-fischer in https://github.com/netbirdio/netbird/pull/5842
* [client] Update `RaceDial` to accept context for improved cancellation by @pappz in https://github.com/netbirdio/netbird/pull/5849
* [management] add domain and service cleanup migration by @pascal-fischer in https://github.com/netbirdio/netbird/pull/5850
* [client] Fix Android internet blackhole caused by stale route re-injection on TUN rebuild by @pappz in https://github.com/netbirdio/netbird/pull/5865
* [client] Fix/grpc retry by @pappz in https://github.com/netbirdio/netbird/pull/5750
* [client] Fix DNS resolution with userspace WireGuard and kernel firewall by @lixmal in https://github.com/netbirdio/netbird/pull/5873


**Full Changelog**: https://github.com/netbirdio/netbird/compare/v0.68.1...v0.68.2

## [v0.68.1] - 2026-04-08

### Changed
- Updated to NetBird v0.68.1

### Upstream Release Notes
## What's Changed
* [client] Include service.json in debug bundle by @lixmal in https://github.com/netbirdio/netbird/pull/5825
* [client] Fix FreeBSD not reporting network addresses by @lixmal in https://github.com/netbirdio/netbird/pull/5827
* [client] Handle UPnP routers that only support permanent leases by @lixmal in https://github.com/netbirdio/netbird/pull/5826
* [management] use NullBool for terminated flag by @pascal-fischer in https://github.com/netbirdio/netbird/pull/5829


**Full Changelog**: https://github.com/netbirdio/netbird/compare/v0.68.0...v0.68.1

## [v0.68.0] - 2026-04-08

### Changed
- Updated to NetBird v0.68.0

### Upstream Release Notes
## What's Changed
* [proxy] Update package-lock.json by @heisbrot in https://github.com/netbirdio/netbird/pull/5661
* [client] Unexport GetServerPublicKey, add HealthCheck method by @pappz in https://github.com/netbirdio/netbird/pull/5735
* [client] Fix mgmProber interface to match unexported GetServerPublicKey by @pappz in https://github.com/netbirdio/netbird/pull/5815
* [management] validate permissions on groups read with name by @pascal-fischer in https://github.com/netbirdio/netbird/pull/5749
* [management] Fix missing service columns in pgx account loader by @lixmal in https://github.com/netbirdio/netbird/pull/5816
* [client] Error out on netbird expose when block inbound is enabled by @lixmal in https://github.com/netbirdio/netbird/pull/5818
* [client] Skip down interfaces in network address collection for posture checks by @lixmal in https://github.com/netbirdio/netbird/pull/5768
* [client] Fix SSH server Stop() deadlock with active sessions by @lixmal in https://github.com/netbirdio/netbird/pull/5717
* [client] Add TCP DNS support for local listener by @lixmal in https://github.com/netbirdio/netbird/pull/5758
* [client] Fix iOS DNS upstream routing for deselected exit nodes by @mlsmaycon in https://github.com/netbirdio/netbird/pull/5803
* [client] Add NAT-PMP/UPnP support by @lixmal in https://github.com/netbirdio/netbird/pull/5202
* [relay] Replace net.Conn with context-aware Conn interface by @pappz in https://github.com/netbirdio/netbird/pull/5770
* [client] Fix SSH proxy mangling shell quoting in forwarded commands by @lixmal in https://github.com/netbirdio/netbird/pull/5669
* [client] Don't abort UI debug bundle when up/down fails by @lixmal in https://github.com/netbirdio/netbird/pull/5780


**Full Changelog**: https://github.com/netbirdio/netbird/compare/v0.67.4...v0.68.0

## [v0.67.4] - 2026-04-05

### Changed
- Updated to NetBird v0.67.4

### Upstream Release Notes
## What's Changed
* [client] Fix flaky TestServiceLifecycle/Restart on FreeBSD by @lixmal in https://github.com/netbirdio/netbird/pull/5786
* [client] Add GetSelectedClientRoutes to route manager and update DNS route check by @mlsmaycon in https://github.com/netbirdio/netbird/pull/5802


**Full Changelog**: https://github.com/netbirdio/netbird/compare/v0.67.3...v0.67.4

## [v0.67.3] - 2026-04-02

### Changed
- Updated to NetBird v0.67.3

### Upstream Release Notes
## What's Changed
* [management] Allow updating embedded IdP user name and email by @bcmmbaga in https://github.com/netbirdio/netbird/pull/5721
* [management] Fix L4 service creation deadlock on single-connection databases by @lixmal in https://github.com/netbirdio/netbird/pull/5779
* [management,client] Revert gRPC client secret removal by @bcmmbaga in https://github.com/netbirdio/netbird/pull/5781


**Full Changelog**: https://github.com/netbirdio/netbird/compare/v0.67.2...v0.67.3

## [v0.67.2] - 2026-04-01

### Changed
- Updated to NetBird v0.67.2

### Upstream Release Notes
## Release Notes for v0.67.2

### What's New
#### Client Improvements
- Added **Expose support to embed library**.  
  https://github.com/netbirdio/netbird/pull/5695
- Persisted **service install parameters across reinstalls**.  
  https://github.com/netbirdio/netbird/pull/5732
- Fixed **Exit Node submenu separator accumulation on Windows**.  
  https://github.com/netbirdio/netbird/pull/5691
- Fixed **Android DNS routes lost after TUN rebuild**.  
  https://github.com/netbirdio/netbird/pull/5739
- Fixed **flaky TestUpdateOldManagementURL in CI**.  
  https://github.com/netbirdio/netbird/pull/5703
- Fixed **path join issue in Windows tests**.  
  https://github.com/netbirdio/netbird/pull/5762
- Fixed **IPv6 address handling in QUIC server**.  
  https://github.com/netbirdio/netbird/pull/5763
- Refactored **Android PeerInfo to use ConnStatus enum**.  
  https://github.com/netbirdio/netbird/pull/5644
- Added support for **embed.Client on Android with netstack mode**.  
  https://github.com/netbirdio/netbird/pull/5623

#### Management Improvements
- Added **notification endpoints**.  
  https://github.com/netbirdio/netbird/pull/5590
- Added **terminated field to services**.  
  https://github.com/netbirdio/netbird/pull/5700
- Extended **blackbox tests**.  
  https://github.com/netbirdio/netbird/pull/5699
- Updated to latest **gRPC version**.  
  https://github.com/netbirdio/netbird/pull/5716
- Prevented **events for temporary peers**.  
  https://github.com/netbirdio/netbird/pull/5719
- Persisted **proxy capabilities to database**.  
  https://github.com/netbirdio/netbird/pull/5720
- Added **FleetDM API spec support**.  
  https://github.com/netbirdio/netbird/pull/5597
- Added **target user account validation**.  
  https://github.com/netbirdio/netbird/pull/5741
- Improved **permission validation for posture check delete**.  
  https://github.com/netbirdio/netbird/pull/5742
- Removed **client secret from gRPC auth flow**.  
  https://github.com/netbirdio/netbird/pull/5751
- Fixed **panic on management reboot**.  
  https://github.com/netbirdio/netbird/pull/5759
- Added **legacy to embedded IdP migration tool**.  
  https://github.com/netbirdio/netbird/pull/5586
- Fixed **race condition in setup flow allowing multiple owners**.  
  https://github.com/netbirdio/netbird/pull/5754

#### Proxy Enhancements
- Added **pprof support** for proxy debugging.  
  https://github.com/netbirdio/netbird/pull/5764

#### Security & Stability
- Added **path traversal and file size protections**.  
  https://github.com/netbirdio/netbird/pull/5755

#### Self-Hosted Improvements
- Added **self-hosted scaling note**.  
  https://github.com/netbirdio/netbird/pull/5769

#### Miscellaneous
- Added **missing OpenAPI definitions**.  
  https://github.com/netbirdio/netbird/pull/5690
- Updated **Contributor License Agreement document**.  
  https://github.com/netbirdio/netbird/pull/5131
- Set **permissions on env file for getting started scripts**.  
  https://github.com/netbirdio/netbird/pull/5761

### New Contributors
- @tobsec made their first contribution in https://github.com/netbirdio/netbird/pull/5691
- @iakshayubale made their first contribution in https://github.com/netbirdio/netbird/pull/5644

**Full Changelog**: https://github.com/netbirdio/netbird/compare/v0.67.1...v0.67.2

## [v0.67.1] - 2026-03-26

### Changed
- Updated to NetBird v0.67.1

### Upstream Release Notes
## What's Changed
* [client] Don't abort debug for command when up/down fails by @lixmal in https://github.com/netbirdio/netbird/pull/5657
* [misc] Set signing env only if not fork and set license by @mlsmaycon in https://github.com/netbirdio/netbird/pull/5659
* [management] Omit proxy_protocol from API response when false by @lixmal in https://github.com/netbirdio/netbird/pull/5656
* [management] Replace JumpCloud SDK with direct HTTP calls by @bcmmbaga in https://github.com/netbirdio/netbird/pull/5591
* [management] Allow multiple header auths with same header name by @lixmal in https://github.com/netbirdio/netbird/pull/5678
* [management] Fix DNS label uniqueness check on peer rename by @bcmmbaga in https://github.com/netbirdio/netbird/pull/5679
* [misc] Replace discontinued LocalStack with MinIO in S3 test by @lixmal in https://github.com/netbirdio/netbird/pull/5680
* [client] Bump go-m1cpu to v0.2.1 to fix segfault on macOS 26 / M5 chips by @lixmal in https://github.com/netbirdio/netbird/pull/5701
* [infrastructure] Enable RPM package gpgcheck in install script by @lixmal in https://github.com/netbirdio/netbird/pull/5676
* [client] Replace iOS DNS IsPrivate heuristic with route checker by @lixmal in https://github.com/netbirdio/netbird/pull/5694


**Full Changelog**: https://github.com/netbirdio/netbird/compare/v0.67.0...v0.67.1

## [v0.67.0] - 2026-03-23

### Changed
- Updated to NetBird v0.67.0

### Upstream Release Notes
## Release Notes for v0.67.0

### What's New
#### Major Networking & Proxy Enhancements
- Introduced **Layer 4 (L4) capabilities (TLS/TCP/UDP)** across client, management, and proxy.  
  https://github.com/netbirdio/netbird/pull/5530
- Added **header-based authentication, access restrictions, and session idle timeout** for proxy services.  
  https://github.com/netbirdio/netbird/pull/5587
- Added support for **wildcard certificates** and improved certificate handling (read from disk if available).  
  https://github.com/netbirdio/netbird/pull/5583  
  https://github.com/netbirdio/netbird/pull/5574
- Added **require_subdomain capability** for proxy clusters.  
  https://github.com/netbirdio/netbird/pull/5628
- Improved proxy reliability with **domain switching fixes and recovery after cleanup**.  
  https://github.com/netbirdio/netbird/pull/5585  
  https://github.com/netbirdio/netbird/pull/5617

> Dashboard support and documentation update are coming soon.

#### Client Improvements
- Added **client metrics support** and enhanced observability.  
  https://github.com/netbirdio/netbird/pull/5512
- Added **health check flag** and daemon status output to `netbird status`.  
  https://github.com/netbirdio/netbird/pull/5650
- Restart engine automatically when **peer IP changes**.  
  https://github.com/netbirdio/netbird/pull/5614
- Improved **DNS handling, IPv6 formatting, and probe thread safety**.  
  https://github.com/netbirdio/netbird/pull/5603  
  https://github.com/netbirdio/netbird/pull/5576
- Added **MTU option and DNSLabels support** to embedded client.  
  https://github.com/netbirdio/netbird/pull/5550  
  https://github.com/netbirdio/netbird/pull/5493
- Refactored **auto-update workflow** and simplified container entrypoint.  
  https://github.com/netbirdio/netbird/pull/5448  
  https://github.com/netbirdio/netbird/pull/5652
- Fixed multiple issues including **duplicate logs, firewall init behavior, and container logging**.  
  https://github.com/netbirdio/netbird/pull/5609  
  https://github.com/netbirdio/netbird/pull/5621

#### Management Improvements
- Added **reverse proxy cluster APIs and domain-based targeting**.  
  https://github.com/netbirdio/netbird/pull/5611  
  https://github.com/netbirdio/netbird/pull/5612
- Improved **concurrency handling and proxy exclusions from peer approval**.  
  https://github.com/netbirdio/netbird/pull/5584  
  https://github.com/netbirdio/netbird/pull/5588

#### Proxy Enhancements
- Added **log-level flag and usage improvements**.  
  https://github.com/netbirdio/netbird/pull/5594

#### Security & Packaging
- Added **GPG signing key support for RPM packages**.  
  https://github.com/netbirdio/netbird/pull/5581

#### Miscellaneous
- Added **image build after merge to main** workflow.  
  https://github.com/netbirdio/netbird/pull/5605
- Added **netbird-tui** to community projects.  
  https://github.com/netbirdio/netbird/pull/5568

### New Contributors
- @n0pashkov made their first contribution in https://github.com/netbirdio/netbird/pull/5568
- @tham-le made their first contribution in https://github.com/netbirdio/netbird/pull/5550
- @wehagy made their first contribution in https://github.com/netbirdio/netbird/pull/5447
- @mango766 made their first contribution in https://github.com/netbirdio/netbird/pull/5603
- @Wouter0100 made their first contribution in https://github.com/netbirdio/netbird/pull/5493

**Full Changelog**: https://github.com/netbirdio/netbird/compare/v0.66.4...v0.67.0

## [v0.66.4] - 2026-03-11

### Changed
- Updated to NetBird v0.66.4

### Upstream Release Notes
## Release Notes for v0.66.4

### What's New

#### Management Improvements
- Create a **shallow copy of the account when buffering** to improve memory safety and performance.  
  https://github.com/netbirdio/netbird/pull/5572

- Set **network map components by default** and optimize **memory usage**.  
  https://github.com/netbirdio/netbird/pull/5575

#### Self-Hosted Improvements
- Removed **extra proxy domain instructions** from the getting started guide to simplify setup.  
  https://github.com/netbirdio/netbird/pull/5573


**Full Changelog**: https://github.com/netbirdio/netbird/compare/v0.66.3...v0.66.4

## [v0.66.3] - 2026-03-09

### Changed
- Updated to NetBird v0.66.3

### Upstream Release Notes
## Release Notes for v0.66.3

### What's New
#### Client Improvements
- Fixed **"reset connection" error after wake from sleep** to improve reconnection stability.  
  https://github.com/netbirdio/netbird/pull/5522
- Fixed **exit node menu not refreshing on Windows**.  
  https://github.com/netbirdio/netbird/pull/5553

#### Management Improvements
- Added **per-target options to the reverse proxy** (management + proxy).  
  https://github.com/netbirdio/netbird/pull/5501
- Avoided breaking **single account mode when switching domains**.  
  https://github.com/netbirdio/netbird/pull/5511
- Added **stable domain resolution for the combined server**.  
  https://github.com/netbirdio/netbird/pull/5515
- Fixed **domain uniqueness validation**.  
  https://github.com/netbirdio/netbird/pull/5529
- Added **activity events for domain operations**.  
  https://github.com/netbirdio/netbird/pull/5548
- Switched proxy registration to use **real IP address**.  
  https://github.com/netbirdio/netbird/pull/5525
- Cached **PKCE state** to improve login flow reliability.  
  https://github.com/netbirdio/netbird/pull/5516
- Count **login request duration metrics only for successful logins**.  
  https://github.com/netbirdio/netbird/pull/5545
- Aggregated **gRPC metrics by account ID**.  
  https://github.com/netbirdio/netbird/pull/5486

#### Proxy Improvements
- Refactored **proxy metrics** and added **usage logs**.  
  https://github.com/netbirdio/netbird/pull/5533

#### CI & Misc
- Added **PR title validation workflow**.  
  https://github.com/netbirdio/netbird/pull/5503

**Full Changelog**: https://github.com/netbirdio/netbird/compare/v0.66.2...v0.66.3

## [v0.66.2] - 2026-03-04

### Changed
- Updated to NetBird v0.66.2

### Upstream Release Notes
## What's Changed
* [management] Store connected proxies in DB by @pascal-fischer in https://github.com/netbirdio/netbird/pull/5472
* [management] Fix embedded IdP metrics to count local and generic OIDC users by @braginini in https://github.com/netbirdio/netbird/pull/5498
* [client] Fix SSH JWT auth failure with Azure Entra ID iat backdating by @hbzhost in https://github.com/netbirdio/netbird/pull/5471
* [misc] Add ISSUE_TEMPLATE configuration file by @mlsmaycon in https://github.com/netbirdio/netbird/pull/5500
* [management] Replace in-memory expose tracker with SQL-backed operations by @mlsmaycon in https://github.com/netbirdio/netbird/pull/5494

## New Contributors
* @hbzhost made their first contribution in https://github.com/netbirdio/netbird/pull/5471

**Full Changelog**: https://github.com/netbirdio/netbird/compare/v0.66.1...v0.66.2

## [v0.66.1] - 2026-03-03

### Changed
- Updated to NetBird v0.66.1

### Upstream Release Notes
## Release Notes for v0.66.1

### What's New
#### Client Improvements
- Fixed **server mutex being held across `waitForUp` in `Up()`**, preventing potential blocking behavior.  
  [#5460](https://github.com/netbirdio/netbird/pull/5460)
- Fixed **close-of-closed-channel panic** in `ConnectClient` retry loop.  
  [#5470](https://github.com/netbirdio/netbird/pull/5470)
- Fixed **deadlock in route peer status watcher**.  
  [#5489](https://github.com/netbirdio/netbird/pull/5489)
- Fixed **profile config directory permissions**.  
  [#5457](https://github.com/netbirdio/netbird/pull/5457)
- Lowered socket auto-discovery log level from **Info to Debug**.  
  [#5463](https://github.com/netbirdio/netbird/pull/5463)

#### Management Improvements
- Prevented deletion of **groups linked to flow groups**.  
  [#5439](https://github.com/netbirdio/netbird/pull/5439)
- Fixed **user update permission validation**.  
  [#5441](https://github.com/netbirdio/netbird/pull/5441)
- Added **reverse proxy services REST client**.  
  [#5454](https://github.com/netbirdio/netbird/pull/5454)
- Added explicit **target deletion on service removal**.  
  [#5420](https://github.com/netbirdio/netbird/pull/5420)

#### Proxy Improvements
- Flushed buffer immediately to improve **gRPC support**.  
  [#5469](https://github.com/netbirdio/netbird/pull/5469)

#### Self-Hosted Enhancements
- Added support for **Embedded IdP PostgreSQL database**.  
  [#5443](https://github.com/netbirdio/netbird/pull/5443)
- Allowed specifying **SQL file locations** for auth, activity, and main stores.  
  [#5487](https://github.com/netbirdio/netbird/pull/5487)

#### Security
- Upgraded **Alpine Linux** from 3.23.2 to 3.23.3.  
  [#5217](https://github.com/netbirdio/netbird/pull/5217)

### New Contributors
- @artivis made their first contribution in [#5457](https://github.com/netbirdio/netbird/pull/5457)

**Full Changelog**: [v0.66.0...v0.66.1](https://github.com/netbirdio/netbird/compare/v0.66.0...v0.66.1)

## [v0.66.0] - 2026-02-24

### Changed
- Updated to NetBird v0.66.0

### Upstream Release Notes
## Release Notes for v0.66.0

## 🚀 New Feature: `netbird expose`

We're excited to introduce **`netbird expose`** --- a simple and secure way to expose your local services through the NetBird reverse proxy.

### ⚡ Expose Local Services with Protection

Expose a local HTTP server:

``` bash
netbird expose 8080
```

This instantly publishes your local service via NetBird's reverse proxy.

You can enhance the exposure with built-in protection and customization:

### 🔐 With PIN protection (6 digits)

``` bash
netbird expose 3000 --with-pin 123456
```

### 🔑 With password protection and name prefix

``` bash
netbird expose 8080 --with-password my-secret --with-name-prefix my-app
```

### 👥 Restrict by SSO user groups

``` bash
netbird expose 8080 --with-user-groups engineering,devops
```

### 🌐 Use a custom domain (pre-configured in your account)

``` bash
netbird expose 8080 --with-custom-domain app.example.com
```

### Supported Flags

-   `--with-pin string` --- Protect the exposed service with a 6-digit
    PIN\
-   `--with-password string` --- Add password protection\
-   `--with-user-groups strings` --- Restrict access to specific user
    groups\
-   `--with-custom-domain string` --- Specify a custom domain\
-   `--with-name-prefix string` --- Prefix the generated service name\
-   `--protocol string` --- Protocol to use (`http` or `https`, default
    `http`)

> :warning: NetBird Cloud support is coming soon with hosted proxy nodes. :warning:

Learn more at: https://docs.netbird.io/manage/reverse-proxy/expose-from-cli

Or watch the video below:
[![Watch the video](https://img.youtube.com/vi/dBPPPloqwcU/0.jpg)](https://youtu.be/dBPPPloqwcU)

#### Client Improvements
- Stopped upstream retry loop immediately on **context cancellation**.  
  [#5403](https://github.com/netbirdio/netbird/pull/5403)
- Fixed **busy-loop in network monitor routing socket** on macOS/BSD.  
  [#5424](https://github.com/netbirdio/netbird/pull/5424)
- Fixed **missed sleep/wakeup events on macOS**.  
  [#5418](https://github.com/netbirdio/netbird/pull/5418)
- Removed **connection semaphore** to simplify connection handling.  
  [#5419](https://github.com/netbirdio/netbird/pull/5419)
- Skipped **UAPI listener in netstack mode**.  
  [#5397](https://github.com/netbirdio/netbird/pull/5397)
- Simplified **DNS logging** by removing domain list from log output.  
  [#5396](https://github.com/netbirdio/netbird/pull/5396)
- Excluded **Flow domain from caching** to prevent TLS failures.  
  [#5433](https://github.com/netbirdio/netbird/pull/5433)
- Added **non-default socket file discovery** support.  
  [#5425](https://github.com/netbirdio/netbird/pull/5425)

#### Client Service Expose
- Introduced **client service expose feature** across client and management.  
  [#5411](https://github.com/netbirdio/netbird/pull/5411)
- Refactored expose feature by moving **business logic from gRPC to manager layer**.  
  [#5435](https://github.com/netbirdio/netbird/pull/5435)

#### Proxy Improvements
- Added **access log cleanup**.  
  [#5376](https://github.com/netbirdio/netbird/pull/5376)
- Implemented **access log sorting**.  
  [#5378](https://github.com/netbirdio/netbird/pull/5378)
- Sent **proxy updates on account deletion**.  
  [#5375](https://github.com/netbirdio/netbird/pull/5375)
- Added **pre-shared key (PSK) support** to proxy.  
  [#5377](https://github.com/netbirdio/netbird/pull/5377)

#### Management Improvements
- Refactored **network map component assembly**.  
  [#5193](https://github.com/netbirdio/netbird/pull/5193)
- Added **custom domain counts and service metrics** to self-hosted metrics.  
  [#5414](https://github.com/netbirdio/netbird/pull/5414)

#### Self-Hosted Enhancements
- Added support for **activity store engine** in the combined server.  
  [#5406](https://github.com/netbirdio/netbird/pull/5406)
- Added **Embedded IdP metrics** for improved observability.  
  [#5407](https://github.com/netbirdio/netbird/pull/5407)

**Full Changelog**: [v0.65.3...v0.66.0](https://github.com/netbirdio/netbird/compare/v0.65.3...v0.66.0)

## [v0.65.3] - 2026-02-19

### Changed
- Updated to NetBird v0.65.3

### Upstream Release Notes
## Release Notes for v0.65.3

🛡️ Security Fix: Race Condition in Role Update Validation





**What was affected**

A race condition in the user role validation logic could allow permission checks to succeed based on stale role data. Under very specific timing conditions, concurrent requests during a role change (e.g., while an admin was being demoted to user) could bypass role validation when changing another users role.

**Exploit Potential**

If an administrator account was being demoted while simultaneously performing acocunt ownership transfer actions, a race window existed where the system could treat the user as having elevated permissions to change owners.

In a coordinated scenario involving two administrator accounts, this could potentially allow privilege escalation — for example, promoting a user to Owner during the demotion window.

**Conditions Required**

Exploitation required:

- Two administrator accounts.
- One administrator being actively demoted.
- Concurrent ownership transfer requests executed precisely during the demotion process.
- Precise timing to trigger the race condition.

This issue required intentional coordination and timing, making it unlikely to occur accidentally and will require access to two admin accounts.

### What's New
#### Client & Mobile Improvements
- Batched **macOS DNS domains** to avoid truncation issues.  
  [#5368](https://github.com/netbirdio/netbird/pull/5368)
- Ensured **route settlement on iOS** before handling DNS responses.  
  [#5360](https://github.com/netbirdio/netbird/pull/5360)
- Added logging of **lock acquisition time** in message handling for improved observability.  
  [#5393](https://github.com/netbirdio/netbird/pull/5393)

#### Relay Improvements
- Reduced **QUIC initial packet size to 1280 bytes** (IPv6 minimum MTU) for better compatibility.  
  [#5374](https://github.com/netbirdio/netbird/pull/5374)

#### Management Improvements
- Fixed possible **race condition on user role change**.  
  [#5395](https://github.com/netbirdio/netbird/pull/5395)
- Added **docker login step** in management tests.  
  [#5323](https://github.com/netbirdio/netbird/pull/5323)

#### Self-Hosted Updates
- Added a **migration script** for upgrading from pre-v0.65.0 to post-v0.65.0 combined setup.  
  [#5350](https://github.com/netbirdio/netbird/pull/5350)
- Removed unused **configuration example** from self-hosted setup.  
  [#5383](https://github.com/netbirdio/netbird/pull/5383)

#### Miscellaneous
- Updated **timestamp format to include milliseconds**.  
  [#5387](https://github.com/netbirdio/netbird/pull/5387)

**Full Changelog**: [v0.65.2...v0.65.3](https://github.com/netbirdio/netbird/compare/v0.65.2...v0.65.3)

## [v0.65.2] - 2026-02-17

### Changed
- Updated to NetBird v0.65.2

### Upstream Release Notes
## Release Notes for v0.65.2

### What's New
#### Client Improvements
- Optimized **Windows DNS performance** with domain batching and batch mode.  
  [#5264](https://github.com/netbirdio/netbird/pull/5264)
- Reset **WireGuard endpoint** on ICE session changes during relay fallback.  
  [#5283](https://github.com/netbirdio/netbird/pull/5283)
- Refactored **WireGuard endpoint setup** with role-based proxy activation.  
  [#5277](https://github.com/netbirdio/netbird/pull/5277)
- Exported **lazy connection environment variables** for mobile clients.  
  [#5310](https://github.com/netbirdio/netbird/pull/5310)
- Ignored false positive **lint alert** in client code.  
  [#5370](https://github.com/netbirdio/netbird/pull/5370)

#### Proxy & Reverse Proxy
- Added **listener-side Proxy Protocol support** and enabled it in Traefik.  
  [#5332](https://github.com/netbirdio/netbird/pull/5332)
- Added **WebSocket support** to the proxy.  
  [#5312](https://github.com/netbirdio/netbird/pull/5312)
- Removed unused **OIDC config flags** from proxy configuration.  
  [#5369](https://github.com/netbirdio/netbird/pull/5369)
- Infrastructure updates for **proxy components**.  
  [#5365](https://github.com/netbirdio/netbird/pull/5365)

#### Management Improvements
- Fixed **UTC difference issue** in peer “last seen” status.  
  [#5348](https://github.com/netbirdio/netbird/pull/5348)
- Ensured **Management starts even if external IdP is down**.  
  [#5367](https://github.com/netbirdio/netbird/pull/5367)
- Added flag to **disable the legacy gRPC endpoint**.  
  [#5372](https://github.com/netbirdio/netbird/pull/5372)

#### Documentation & Misc
- Added additional **proxy domain instructions**.  
  [#5328](https://github.com/netbirdio/netbird/pull/5328)
- Added an extra **CNAME configuration example**.  
  [#5341](https://github.com/netbirdio/netbird/pull/5341)

**Full Changelog**: [v0.65.1...v0.65.2](https://github.com/netbirdio/netbird/compare/v0.65.1...v0.65.2)

## [v0.65.1] - 2026-02-14

### Changed
- Updated to NetBird v0.65.1

### Upstream Release Notes
## What's Changed
* [misc] Fix reverse proxy getting started messaging by @braginini in https://github.com/netbirdio/netbird/pull/5317
* [management] Move service reload outside transaction in account settings update by @bcmmbaga in https://github.com/netbirdio/netbird/pull/5325


**Full Changelog**: https://github.com/netbirdio/netbird/compare/v0.65.0...v0.65.1

## [v0.65.0] - 2026-02-13

### Changed
- Updated to NetBird v0.65.0

### Upstream Release Notes
# Release Notes for v0.65.0

## What's New

### 🔀 Reverse Proxy

NetBird now includes a built-in reverse proxy in the management server, enabling proxied access to backend services through your NetBird network. Allowing you to expose your services to the public with the option to secure them with SSO, PINs, or passwords.

No VPN client required for end users. Just point a custom domain at your NetBird server, configure the proxy in the dashboard, and your internal services are securely accessible from any browser. Think of it as a self-hosted alternative to Cloudflare Tunnels, but without the MITM and fully under your control.

**Key features:**

* **Custom domains** - Map your own domains to internal services and let NetBird handle TLS and routing via CNAME verification
* **Built-in authentication** - Protect exposed services with SSO (via your configured IdP), PIN codes, passwords, or magic links directly from the dashboard
* **Multiple targets** - Route traffic to one or more backend peers or resources with optional path-based routing
* **Access logs** - Monitor who's accessing your proxied services with built-in logging
* **Proxy settings** - Fine-tune behavior with options like host header passthrough and redirect rewriting

#### Add a Service

Expose any internal service by selecting a subdomain and adding one or more backend targets. Each target points to a peer or resource on your network.

<img width="400" height="400" alt="image" src="https://github.com/user-attachments/assets/3bd8b332-a49d-4f3e-ba67-b95615b362ca" />


<img width="400" height="400" alt="image" src="https://github.com/user-attachments/assets/0ca780b9-5a10-406b-ae72-4a84586f8dfd" />

#### Custom Domains

Bring your own domain by adding a CNAME record pointing to your NetBird proxy cluster. NetBird handles TLS certificate provisioning automatically.

<img width="400" height="400" alt="image" src="https://github.com/user-attachments/assets/9d162966-7815-4bd2-a2dd-1993e13ae891" />

#### Authentication

Secure your exposed services with multiple authentication methods. Enable one or combine several for layered protection.

<img width="400" height="400" alt="image" src="https://github.com/user-attachments/assets/fd385a87-f7fd-41c0-8998-fe00113d8e57" />


#### Settings

Fine-tune proxy behavior with options like passing the original Host header to your backend or rewriting redirect URLs to use the public domain.

<img width="400" height="400" alt="image" src="https://github.com/user-attachments/assets/1b19c92c-1f8b-40ce-a8ce-a30f21ec5d0d" />

Learn more:
* [Reverse Proxy Overview](https://docs.netbird.io/manage/reverse-proxy)
* [Custom Domains](https://docs.netbird.io/manage/reverse-proxy/custom-domains)
* [Authentication](https://docs.netbird.io/manage/reverse-proxy/authentication)

> NetBird cloud support is coming soon, with hosted reverse proxy nodes.


### 🏗️ Self-Hosted Improvements

* Added **combined NetBird server** binary for simplified self-hosted deployments, reducing the number of containers needed to run NetBird.
  [#5232](https://github.com/netbirdio/netbird/pull/5232)

### 🔒 Management Improvements

* **Enforced access control on accessible peers**, ensuring proper authorization checks when querying the accessible peers endpoint.
  [#5301](https://github.com/netbirdio/netbird/pull/5301)
* Added **cloud API spec to the public OpenAPI** definition with REST client support.
  [#5222](https://github.com/netbirdio/netbird/pull/5222)

### 🖥️ Client Improvements

* Added **early message buffer for the relay client**, preventing message loss during connection establishment.
  [#5282](https://github.com/netbirdio/netbird/pull/5282)
* **Refactored relay connection container** for improved reliability and code maintainability.
  [#5271](https://github.com/netbirdio/netbird/pull/5271)

## What's Changed

* [misc] Update sign pipeline version by @mlsmaycon in [#5296](https://github.com/netbirdio/netbird/pull/5296)
* [self-hosted] add netbird server by @braginini in [#5232](https://github.com/netbirdio/netbird/pull/5232)
* [management] Enforce access control on accessible peers by @bcmmbaga in [#5301](https://github.com/netbirdio/netbird/pull/5301)
* [misc] Add cloud api spec to public open api with rest client by @bcmmbaga in [#5222](https://github.com/netbirdio/netbird/pull/5222)
* [client] Add early message buffer for relay client by @pappz in [#5282](https://github.com/netbirdio/netbird/pull/5282)
* [client] Refactor/relay conn container by @pappz in [#5271](https://github.com/netbirdio/netbird/pull/5271)
* [management, reverse proxy] Add reverse proxy feature by @pascal-fischer in [#5291](https://github.com/netbirdio/netbird/pull/5291)

**Full Changelog**: [v0.64.6...v0.65.0](https://github.com/netbirdio/netbird/compare/v0.64.6...v0.65.0)

## [v0.64.6] - 2026-02-12

### Changed
- Updated to NetBird v0.64.6

### Upstream Release Notes
## Release Notes for v0.64.6

### What's New

🚨 Security Fix
Security: Fixed account impersonation validation in management API

Fixed a vulnerability in the management server's authentication middleware where the ?account= query parameter could be used to impersonate arbitrary accounts without proper validation when getting a list of accessible peers. It requires the attacker to have prior knowledge of the target accounts' and peer IDs. 

The fix adds explicit validation via IsValidChildAccount() before allowing account switching. Account impersonation is now only permitted when the target account is confirmed as a legitimate child account of the
  requesting user's parent account.

Affected component: Management server HTTP middleware (auth_middleware.go) and `/api/peers/<peer_id>/accessible-peers` endpoint

Severity: High — an authenticated user could potentially access or act on behalf of accounts they should not have access to by passing an arbitrary account parameter and fetching the list of accessible peers.

**Recommendation**: All self-hosted deployments should upgrade to this version.

#### Client Improvements
- Added **missing BSD flags** to the debug bundle.  
  [#5254](https://github.com/netbirdio/netbird/pull/5254)
- Cached the result of `wgInterface.ToInterface()` using `sync.Once` for better performance.  
  [#5256](https://github.com/netbirdio/netbird/pull/5256)
- Fixed **nil pointer panic** in the ICE agent during sleep/wake cycles.  
  [#5261](https://github.com/netbirdio/netbird/pull/5261)
- Always log **DNS forwarder responses** for improved troubleshooting.  
  [#5262](https://github.com/netbirdio/netbird/pull/5262)
- Fixed **netstack detection** and added a **WireGuard port option**.  
  [#5251](https://github.com/netbirdio/netbird/pull/5251)
- Corrected wrong URL logging for `DefaultAdminURL`.  
  [#5252](https://github.com/netbirdio/netbird/pull/5252)
- Added **timing measurements** to `handleSync` for better observability.  
  [#5228](https://github.com/netbirdio/netbird/pull/5228)
- Fixed duplicate firewall rules in **USP filter**.  
  [#5269](https://github.com/netbirdio/netbird/pull/5269)
- Added environment variable to **skip DNS probing** when needed.  
  [#5270](https://github.com/netbirdio/netbird/pull/5270)
- Fixed race condition and ensured correct **message ordering in Relay**.  
  [#5265](https://github.com/netbirdio/netbird/pull/5265)
- Ensured login is checked in **foreground mode** when required.  
  [#5295](https://github.com/netbirdio/netbird/pull/5295)
- Fixed multiple **panics in device and engine code**.  
  [#5287](https://github.com/netbirdio/netbird/pull/5287)
- Cleaned up **stale nftables entries without handle**.  
  [#5272](https://github.com/netbirdio/netbird/pull/5272)

#### Management Improvements
- Fixed incorrectly setting **disconnected status** for connected peers.  
  [#5247](https://github.com/netbirdio/netbird/pull/5247)
- Added **gRPC debounce for message types** to reduce noise.  
  [#5239](https://github.com/netbirdio/netbird/pull/5239)
- Added validation of **stream start time** for connecting peers.  
  [#5267](https://github.com/netbirdio/netbird/pull/5267)
- Fixed `ischild` check logic.  
  [#5279](https://github.com/netbirdio/netbird/pull/5279)

### New Contributors
- @eyJhb made their first contribution in [#5252](https://github.com/netbirdio/netbird/pull/5252)

**Full Changelog**: [v0.64.5...v0.64.6](https://github.com/netbirdio/netbird/compare/v0.64.5...v0.64.6)

## [v0.64.5] - 2026-02-03

### Changed
- Updated to NetBird v0.64.5

### Upstream Release Notes
## What's Changed
* Add selfhosting video by @braginini in https://github.com/netbirdio/netbird/pull/5235
* [management] adding account id validation to accessible peers handler by @pascal-fischer in https://github.com/netbirdio/netbird/pull/5246


**Full Changelog**: https://github.com/netbirdio/netbird/compare/v0.64.4...v0.64.5

## [v0.64.4] - 2026-02-01

### Changed
- Updated to NetBird v0.64.4

### Upstream Release Notes
## What's Changed
* [client] Add macOS default resolvers as fallback by @lixmal in https://github.com/netbirdio/netbird/pull/5201
* [client] Add block inbound option to the embed client by @lixmal in https://github.com/netbirdio/netbird/pull/5215
* [management] Disable local users for a smooth single-idp mode by @braginini in https://github.com/netbirdio/netbird/pull/5226
* [management] disable sync lim by @crn4 in https://github.com/netbirdio/netbird/pull/5233
* [management] run cancelPeerRoutines in goroutine in sync by @crn4 in https://github.com/netbirdio/netbird/pull/5234


**Full Changelog**: https://github.com/netbirdio/netbird/compare/v0.64.3...v0.64.4

## [v0.64.3] - 2026-01-29

### Changed
- Updated to NetBird v0.64.3

### Upstream Release Notes
## What's Changed
* [client] Remove redundant square bracket trimming in USP endpoint parsing by @pappz in https://github.com/netbirdio/netbird/pull/5197
* [client] Refactor/optimise raw socket headers by @pappz in https://github.com/netbirdio/netbird/pull/5174
* [management] fix ephemeral peers being not removed by @crn4 in https://github.com/netbirdio/netbird/pull/5203
* [management] fix skip of ephemeral peers on deletion by @crn4 in https://github.com/netbirdio/netbird/pull/5206
* [client] Stop NetBird on firewall init failure by @lixmal in https://github.com/netbirdio/netbird/pull/5208
* [management] Streamline domain validation by @lixmal in https://github.com/netbirdio/netbird/pull/5211
* [client] Fix WG watcher missing initial handshake by @pappz in https://github.com/netbirdio/netbird/pull/5213


**Full Changelog**: https://github.com/netbirdio/netbird/compare/v0.64.2...v0.64.3

## [v0.64.2] - 2026-01-27

### Changed
- Updated to NetBird v0.64.2

### Upstream Release Notes
## Release Notes for v0.64.2

### What's New
#### Client Improvements
- Consolidated **authentication logic** to improve maintainability and consistency.  
  [#5010](https://github.com/netbirdio/netbird/pull/5010)
- Added **IPv6 support** to the UDP WireGuard proxy.  
  [#5169](https://github.com/netbirdio/netbird/pull/5169)
- Fixed a **flaky JWT SSH test** to improve CI stability.  
  [#5181](https://github.com/netbirdio/netbird/pull/5181)
- Updated **Fyne UI** and added **retry handling** to the exit menu.  
  [#5187](https://github.com/netbirdio/netbird/pull/5187)
- Prevented **eBPF traffic** from being tracked in conntrack.  
  [#5166](https://github.com/netbirdio/netbird/pull/5166)
- Added support for **non-PTY, no-command interactive SSH sessions**.  
  [#5093](https://github.com/netbirdio/netbird/pull/5093)

#### Management & Identity
- Fixed **validator warning messages** to improve clarity.  
  [#5168](https://github.com/netbirdio/netbird/pull/5168)
- Improved **peer deletion error handling**.  
  [#5188](https://github.com/netbirdio/netbird/pull/5188)
- Included **default groups claim** in the CLI audience.  
  [#5186](https://github.com/netbirdio/netbird/pull/5186)
- Added **user invite link** support for the embedded IdP.  
  [#5157](https://github.com/netbirdio/netbird/pull/5157)


**Full Changelog**: [v0.64.1...v0.64.2](https://github.com/netbirdio/netbird/compare/v0.64.1...v0.64.2)

## [v0.60.2] - 2025-11-17

### Changed
- Updated to NetBird v0.60.2
- **BREAKING**: Removed support for armhf, armv7, and i386 architectures
- Only aarch64 and amd64 architectures are now supported

## [v0.54.2] - 2025-11-17

### Changed
- Updated to NetBird v0.54.2
- Improved security by masking sensitive setup key in logs
- Enhanced error handling in service startup script
- Better documentation for DNS resolver workaround

### Fixed
- Fixed inconsistent addon slug in documentation
- Fixed broken repository links
- Updated maintenance year to 2025
- Corrected default management URL across documentation

### Added
- AppArmor security profile
- Healthcheck configuration for monitoring addon status
- Improved file migration logic with better error handling
- Binary existence check before execution

### Security
- Removed sensitive credential logging
- Added AppArmor profile for enhanced security

## [Unreleased]

### Notes
- Based on hassio-addons base image 19.0.0
- Supports aarch64 and amd64 architectures only
- Requires privileged capabilities for VPN functionality
