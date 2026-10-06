# Changelog

## [fix] - 2026-10-07

### Fixed
- Fixed the `" flowerProcessing"` config key typo that crashed the resource on start (pairs(nil)).
- Server events now re-verify bucket / flower / box requirements before changing the inventory.
- Config.ProcessTime values converted from strings to numbers.
- Fixed undefined playerPed in two ClearPedTasks calls.
