## v0.5.1 to-be-released

### Changed

* relations won't be finalized when table(s) is/are missing (solnic)

### Fixed

* Wrap errors when calling commands with `[]`-syntax (kwando)

[Compare v0.5.0...v0.5.1](https://github.com/rom-rb/rom-sql/compare/v0.5.0...v0.5.1)

## v0.5.0 2015-05-22

### Added

* Association macros support addition `:on` option (solnic)
* `associates` plugin for `Create` command (solnic)
* Support for NotNullConstraintError (solnic)
* Support for UniqueConstraintConstraintError (solnic)
* Support for ForeignKeyConstraintError (solnic)
* Support for CheckConstraintError (solnic)
* `Commands::Update#original` supports objects coercible to_h now (solnic)

### Changed

* [BREAKING] Constraint errors are no longer command errors which means `try` and
  `transaction` blocks will not catch them (solnic)
* `Commands::Update#set` has been deprecated (solnic)
* `Commands::Update#to` has been deprecated (solnic)

[Compare v0.4.3...v0.5.0](https://github.com/rom-rb/rom-sql/compare/v0.4.2...v0.5.0)

## v0.4.3 2015-05-17

### Fixed

* `transaction` doesn't swallow errors now other than CommandError (solnic)

[Compare v0.4.2...v0.4.3](https://github.com/rom-rb/rom-sql/compare/v0.4.2...v0.4.3)

## v0.4.2 2015-05-17

### Added

* Support for setting custom association name (solnic)
* Support for `:conditions` option in association definition (solnic)
* Better error message when accessing undefined associations (pdswan)

### Fixed

* Correct `ROM::SQL::Plugin::Pagination::Pager#total_pages` when total is not
  evenly divisible by page size (larribas)
* `association_join` behaves correctly when dataset is different than register_as (nepalez)

### Changed

* `transaction` returns command failure objects when there was a rollback (solnic)

[Compare v0.4.1...v0.4.2](https://github.com/rom-rb/rom-sql/compare/v0.4.1...v0.4.2)

## v0.4.1 2015-04-04

### Added

* Database error handling for update and delete commands (kwando + solnic)
* Migration interface as a repository plugin (gotar + solnic)

[Compare v0.4.0...v0.4.1](https://github.com/rom-rb/rom-sql/compare/v0.4.0...v0.4.1)

## v0.4.0 2015-03-22

### Added

* `ROM::SQL::Relation` which explictly defines an interface on top of Sequel (solnic + mcls)
* Postgres-specific Create and Update commands that support RETURNING (gotar + solnic)
* `Update#change` interface for skipping execution when there's no diff (solnic)
* Experimental migration API using sequel/migrations (gotar)
* Pagination plugin (solnic)
* Allow reuse of established Sequel connections (splattael)

### Changed

* Use ROM's own inflector which uses either ActiveSupport or Inflecto backends (mjtko)

### Fixed

* Indentation in Rails logger (morgoth)

[Compare v0.3.2...v0.4.0](https://github.com/rom-rb/rom-sql/compare/v0.3.2...v0.4.0)

## v0.3.2 2015-01-01

### Fixed

* Checking tuple count in commands (solnic)

[Compare v0.3.1...v0.3.2](https://github.com/rom-rb/rom-sql/compare/v0.3.1...v0.3.2)

## v0.3.1 2014-12-31

### Added

* `Adapter#disconnect` (solnic)
* Support for extra connection options (solnic)

[Compare v0.3.0...v0.3.1](https://github.com/rom-rb/rom-sql/compare/v0.3.0...v0.3.1)

## v0.3.0 2014-12-19

### Changed

* `association_join` now uses Sequel's `graph` interface which qualifies columns automatically (solnic)
* Delete command returns deleted tuples (solnic)

[Compare v0.2.0...v0.3.0](https://github.com/rom-rb/rom-sql/compare/v0.2.0...v0.3.0)

## v0.2.0 2014-12-06

### Added

* Command API (solnic)
* Support for ActiveSupport::Notifications with a log subscriber (solnic)
* New `ROM::SQL::Adapter#dataset?(name)` checking if a given table exists (solnic)

[Compare v0.1.1...v0.2.0](https://github.com/rom-rb/rom-sql/compare/v0.1.1...v0.2.0)

## v0.1.1 2014-11-24

### Fixed

* Equalizer in header (solnic)

### Changed

* minor refactor in adapter (solnic)

[Compare v0.1.0...v0.1.1](https://github.com/rom-rb/rom-sql/compare/v0.1.0...v0.1.1)

## v0.1.0 2014-11-24

First release powered by Sequel
