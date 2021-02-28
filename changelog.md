# Changelog - "Shot DataBase" Decent DE1app plugin

Format based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/).

## [1.02] - 2021-03-? (Bundled with DE1app 1.34.?)

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