# Version 1.2.6 - 2026-04-16

- Fix ZTS mode, as used by FrankenPHP
- Fix memory leak in excimer_log_get_speedscope_data
- Fix test failure in PHP 8.4

# Version 1.2.5 - 2025-05-19

- Fix build error with libtool 1.5

# Version 1.2.4 - 2025-05-19

- Rewrite the backend to work around a glibc timer aliasing bug (T391426).
  Timer creation and deletion are now more expensive, so applications should
  try to avoid unnecessary creation and deletion. It's cheaper to stop and
  start an existing timer. Handling events is cheaper, so profiling
  performance is improved.
- Compile with -fvisibility=hidden

# Version 1.2.3 - 2024-11-15

- Fix start time stagger, broken by previous release

# Version 1.2.2 - 2024-07-31

- Fix PHP 8.4 compatibility (patch by Remi Collet)

# Version 1.2.1 - 2024-02-29

- Fix compiler warning in excimer_log
- Fix invalid OS requirement in package.xml, allow all "unix"

# Version 1.2.0 - 2024-02-28

- Add support for BSD and macOS (only real/wall-clock, no CPU timer).
- Add excimer.default_max_depth and default to 1000 (previously unlimited).

# Version 1.1.1 - 2023-03-13

- Restore support for PHP 7.1-7.3

# Version 1.1.0 - 2023-03-01

- Fix leading semi-colon in ExcimerLog::formatCollapsed output
- Change ExcimerLog::formatCollapsed to mark truncated frames
- Add support for PHP 8.2
- Add ExcimerLog::getSpeedscopeData for Speedscope support

# Version 1.0.4 - 2022-05-07

- Fix arginfo error for PHP 7.1

# Version 1.0.3 - 2022-05-04

- Set return type on ExcimerLog::aggregateByFunction
- Set return type on ExcimerProfiler::getLog

# Version 1.0.2 - 2021-10-16

- Fix Iterator prototypes for PHP 8.1
- Add extension version in phpinfo()

# Version 1.0.1 - 2021-09-29

- Filter null bytes out of the collapsed output
- Fix segfault in ZTS mode
- Fix [-Wincompatible-pointer-types] with PHP 8

# Version 1.0.0 - 2021-02-26

- Initial PECL release

