# Changelog
All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](http://keepachangelog.com/en/1.0.0/) and this project adheres to [Semantic Versioning](http://semver.org/spec/v2.0.0.html).

## [Unreleased]


## [1.1.0] - 2017-08-08
### Added
- `dateColor`, `dateFont`, `dateSize`, `eventColor`, `eventFont`, `eventSize`, `serverHost`, `textToday`, and `textTomorrow` config options.

### Changed
- Fixed bug with newer versions of Node where token file would not be read in the correct encoding thus causing the plugin to fail.
- If an error happens when trying to get data for a calendar, the error will be displayed at the bottom (above the "about" menu), while the rest of the calendars attempt to load. This way, one calendar failing does not make the rest fail.
- Plugin will now automatically delete the token file and prompt you with re-authorization instructions when re-authorization is needed.
- Switched from `http` to `hapi` for HTTP server.
- CHANGELOG.md formatting.

### Removed
- `fs` npm module as a dependency because we want to use Node's built-in version.


## [1.0.1] - 2017-04-04
### Added
- Support for multiple calendars. (Thanks [@ehershey](https://github.com/ehershey)!)
- startDate option.

### Changed
- Changed showAllOfToday option to showAllOfFirstDay.
- Fixed bug where expanded events would not show up correctly.


## 1.0.0 - 2017-02-23
### Added
- Initial release.

[Unreleased]: https://github.com/kodie/bitbar-googlecal/compare/v1.0.0...HEAD
[1.1.0]: https://github.com/kodie/bitbar-googlecal/compare/v1.0.1...v1.1.0
[1.0.1]: https://github.com/kodie/bitbar-googlecal/compare/v1.0.0...v1.0.1
