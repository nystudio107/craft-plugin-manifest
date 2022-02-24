# Plugin Manifest Changelog

## 4.0.0-beta.1 - 2022.02.24

### Added

* Initial Craft CMS 4 compatibility

## 1.0.8 - 2021.10.11
### Changed
* Handle catching all exceptions, to cover misconfigured installations ([#2](https://github.com/nystudio107/craft-plugin-manifest/issues/2))
* 
## 1.0.7 - 2021.09.22
### Changed
* Remove `Craft::t()` that depended on a translation method that may or may not exist

## 1.0.6 - 2021.08.19
### Changed
* Only do setup in the `ManifestServce::init()` method for CP requests

## 1.0.5 - 2021.07.13
### Changed
* Wrap calls to `is_file()` with try/catch, to handle open_basedir restrictions that cause exceptions to be thrown (https://github.com/nystudio107/craft-seomatic/issues/924)

## 1.0.4 - 2021.05.06
### Fixed
* Don't call any AssetManager methods in the component `init()` method during console requests

## 1.0.3 - 2021.04.07
### Fixed
* Add a `100ms` delay when requesting the manifest file if using it in hot mode, as a hack to avoid a `webpack-dev-server` / Tailwind CSS JIT race condition (https://github.com/nystudio107/craft/issues/55)

## 1.0.2 - 2021.03.21
### Added
* Added a `FileDependency` cache dependency for files loaded from a local path, so things like the `manifest.json` will auto-cache bust if the file changes

### Changed
* Use Guzzle for remote file fetches rather than `curl`, for improved performance

## 1.0.1 - 2021.03.05
### Added
* Added the ability to pass in the environment variable to check for enabling the devServer, so it's not hard-coded at `NYS_PLUGIN_DEVSERVER`

## 1.0.0 - 2021.03.02
### Added
- Initial release
