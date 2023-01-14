# Changelog

Notable changes to the project will be documented in this changelog.

This project uses [Semantic Versioning] and generally follows the conventions of [Keep A Changelog].

## [Unreleased]

Important planned changes not yet bundled up will be listed here.

## [0.4.0] - 2023-01-13

Substantial changes to better support multiple blocklist formats

### Added

- Added support for RapidBlock blocklists, both CSV and JSON formats. (327a44d)
- Added support for per-instance-source import_fields. (327a44d)
- Updated sample config to include new formats. (327a44d)
- A BlockSeverity of 'suspend' implies reject_media and reject_reports. (327a44d)
- Added ability to limit max severity per-URL source. (10011a5)
- Added boolean fields like 'reject_reports' to mergeplan handling. (66f0373)
- Added tests for boolean merge situations. (66f0373)
- Various other test cases added.

### Changed

- Refactored to add a DomainBlock object. (10011a5)
- Refactored to use a BlockParser structure. (10011a5)
- Improved method for checking if changes are needed. (10011a5)
- Refactored fetch from URLs and instances. (327a44d)
- Improved check_followed_severity() behaviour. (327a44d)
- Changed API delay to be in calls per hour. (327a44d)
- Improved comment merging. (0a6eec4)
- Clarified logic in apply_mergeplan() for boolean fields. (66f0373)
- Updated README documentation. (ee9625d)
- Aligned API call rate limit with server default. (55dad3f)

### Removed

- Removed redundant global vars. (327a44d)

### Fixed

- Fixed bug in severity change detection. (e0d40b5)
- Fix DomainBlock.id usage during __iter__() (a718af5)
- 

## [0.3.0] - 2023-01-11

### Added

- Added args to show version information. (1d0649a)
- Added timeout to requests calls. (23b8833)
- Added CHANGELOG.md (ca9d958)

### Changed

- Changed min Python version to v3.10. (f37ab70)

## [0.2.1] - 2023-01-10

### Added

- User-Agent is set to FediBlockHole to identify ourselves to remote servers. (04d9eea)
- Adding packaging to prepare for submission to PyPI. (4ab369f)
- Added ability to set max severity level if an instance has followers of accounts on a to-be-blocked domain. (5518421)
- Added ability to read domain_blocks from instances that make the list public. (4ef84b5)
- Skip obfuscated domains when building the merged blocklist. (4ef84b5)

### Changed

- Updated documentation in README and the sample config. (68a2c93)

### Fixed

- Fixed a bug in config enablement of intermediate blocklists saving. (5518421)

## Before 2023-01-10

- Initial rough versions that were not packaged.

<!-- Links -->
[keep a changelog]: https://keepachangelog.com/en/1.0.0/
[semantic versioning]: https://semver.org/spec/v2.0.0.html

<!-- Versions -->
[unreleased]: https://github.com/eigenmagic/fediblockhole/compare/v0.3.0...HEAD
[0.3.0]: https://github.com/eigenmagic/fediblockhole/releases/tag/v0.2.1
[0.2.1]: https://github.com/eigenmagic/fediblockhole/releases/tag/v0.2.1