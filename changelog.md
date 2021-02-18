# Changelog - "Shot DataBase" Decent DE1app plugin

Format based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/).

## [1.00] - 2021-02-17 (Bundled with DE1app 1.34.11)

### Changed
- Initial code split off the DB namespace from the [DSx DYE plugin](https://github.com/ebengoechea/dye_de1app_dsx_plugin/blob/main/changelog.md).
- Added structure to work as a DE1app plugin instead of a DSx plugin.
- Remade db_close to prevent runtime errors if called more than once.
- Define which procs are namespace-exported.
- New settings 'sync_on_startup' and 'log_sql_statements'.
- Added settings page.