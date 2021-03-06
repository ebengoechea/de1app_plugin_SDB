# Changelog - "Shot DataBase" Decent DE1app plugin

Format based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/).

## [1.06] - 2021-05-08

### Changed
- Don't raise a runtime error if parsing a shot file fails while synchronizing. Only log an error and show the total number of errors in a new line in the settings page
- Sort categories in FSH page by most recently used first
- Move package dependencies to preload to avoid problems when downgrading versions
- Set DYE_settings page through 'dui page add' instead of inside setup


## [1.05] - 2021-04-30

### Changed
- Change the Fontawesome symbol names to standard names.

## [1.04] - 2021-04-29

### Changed 
- Ensure the required minimum version of the DE1app is used (v1.36 for this plugin version)
- Use DUI instead of DGUI to setup the settings page.
- Copy shots.db from the DSx plugin on first install.
- Data dictionary functions are back, now that the DGUI plugin is obsolete.

## [1.03] - 2021-03-29

### Changed 
- Patch bug when $::settings(repository_links) was not initialized.
- Use Jeff K's new events system to hook when a shot is finished.

## [1.02] - 2021-03-01 (Bundled with DE1app 1.34.?)

### Changed 
- Adapt to new plugins and logging systems in 1.34.14
- Define symbols used in the plugin on preload (new DGUI proc set_symbols)

## [1.01] - 2021-02-21 (Bundled with DE1app 1.34.14)

### Changed
- Data dictionary functions moved to DGUI plugin, to avoid circular dependencies.
- `init` proc moved to `main`.
- Handle dependencies using the proposed changes to the extensions system.
- New proc `db_path` returns the path to the database (previously hardcoded).

## [1.00] - 2021-02-17 (Bundled with DE1app 1.34.11)

### Changed
- Initial code split off the DB namespace from the [DSx DYE plugin](https://github.com/ebengoechea/dye_de1app_dsx_plugin/blob/main/changelog.md).
- Added structure to work as a DE1app plugin instead of a DSx plugin.
- Remade `db_close` to prevent runtime errors if called more than once.
- Define which procs are namespace-exported.
- New settings `sync_on_startup` and `log_sql_statements`.
- Added settings page.