# Changelog
All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](http://keepachangelog.com/en/1.0.0/)
and this project adheres to [Semantic Versioning](http://semver.org/spec/v2.0.0.html).

## [Unreleased]

## [2.10.1] - 2020-04-06
### Fixed
- Custom IAM Role name now includes the stage to avoid collision between environments

## [2.10.0] - 2020-04-06
### Added
- Custom IAM Role added to avoid hitting IAM Policy size limit

### Changed
- Sls helper peer dependency changed to 1.9.0 or higher

## [2.9.2] - 2020-03-26
### Fixed
- Escaped error response message to avoid breaking JSON structure

## [2.9.1] - 2020-03-26
### Fixed
- Response template now cleans up superstruct errors

## [2.9.0] - 2020-03-18
### Changed
- NAMING: Lambda functions naming changed to prevent function names to be too long

## [2.8.0] - 2020-03-18
### Added
- Header `janis-entity` is now allowed in CORS configuration

## [2.7.0] - 2020-03-04
### Added
- Support for `ImportExportAuthorizer`

## [2.6.0] - 2020-02-26
### Added
- `package.include` support for event listeners
- Lambda log groups now have a default retention of 14 days

## [2.5.0] - 2020-02-21
### Added
- API Gateway response `AUTHORIZER_CONFIGURATION_ERROR`

### Fixed
- API Gateway responses are not overriden any more

## [2.4.1] - 2020-02-20
### Fixed
- API hook now normalizes the path to avoid bad function naming

## [2.4.0] - 2020-02-19
### Added
- `package.include` support for all API hooks

## [2.3.0] - 2020-02-19
### Added
- `timeout` support for all API hooks
- `functionRawProps` support for all API hooks
- `eventRawProps` support for all API hooks

## [2.2.0] - 2020-02-18
### Added
- Custom authorizer support added in event listeners
- Custom authorizers can now be defined in `custom.authorizers` object in initial config and they will be remain untouched

### Fixed
- Authorizers now use the correct ARN

## [2.1.0] - 2020-02-14
### Added
- Access denied API Gateway response resource added with CORS headers

## [2.0.0] - 2020-02-10
### Added
- `authorizers` now have require the Account ID as a configuration option
- Added the `@janiscommerce/serverless-plugin-remove-authorizer-permissions` serverless plugin to allow cross-account deployments

## [1.3.4] - 2020-02-05
### Fixed
- `authorizers` now have the name property to avoid collisions

## [1.3.3] - 2020-01-22
### Fixed
- `eventListener` hook function name now includes the service name

## [1.3.2] - 2020-01-22
### Fixed
- `base` hook prune plugin typo fix

## [1.3.1] - 2020-01-21
### Fixed
- `eventListener` documentation fixed

## [1.3.0] - 2020-01-16
### Added
- `janis.api` hook added to implement custom APIs

### Changed
- Option `serviceName` changed to `serviceCode` in `janis.base` hook **BREAKING CHANGE**
- Added service name to naming, file path and API path in `janis.eventListener` hook

## [1.2.4] - 2019-12-27
### Fixed
- Authorizers in event listeners are now correctly configured

## [1.2.3] - 2019-12-27
### Fixed
- Authorizers fixed to match the correct function name

## [1.2.2] - 2019-12-26
### Fixed
- Serverless offline cache invalidation regex fixed

## [1.2.1] - 2019-12-26
### Fixed
- Service name in lower case is now in *kebab-case*

## [1.2.0] - 2019-12-26
### Added
- `apiSecrets` configuration in base hook
- Sample service example in README

### Fixed
- `base` documentation updated with required fields

## [1.1.0] - 2019-12-25
### Changed
- Runtime upgraded to nodejs.12x
- Base hook updated to the last configurations
- New authorizers added
- Event listener hook added
