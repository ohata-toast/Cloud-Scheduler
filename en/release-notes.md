# Release Notes

**Application Service > Cloud Scheduler > Release Notes**

## June 24, 2025
### Bug Fixes
* Fixed a bug where parameters (Request Body) had to be entered as JSON objects only.

## May 27, 2025
### Bug Fixes
* Fixed console messages about the time zone applied to the start and end dates.

## April 29, 2025
### Bug Fixes
* Fixed a bug where the schedule execution time was not displayed when a Cron expression was set to every Sunday during schedule creation or editing.

## March 25, 2025
### Added Features
* Added the target template feature

### Feature Updates
* Modified to limit the size of parameters to 256 KB when creating and modifying schedules and templates

## January 21, 2025
### Feature Updates
* Added restrictions when creating schedules
  * Changed the maximum length of a URL to 255 characters when creating and modifying schedules.
  * Changed the maximum size of a parameter to 56 KB when creating and modifying schedules.
  * Changed the start date when creating and modifying schedules to only be set to 5 minutes after the current time.
* Made modifications to ignore spaces before and after search terms when searching for schedules and templates
* Changed error messages

## December 24, 2024
### Added Features
* Added the schedule template feature

## November 26, 2024

### Bug Fixes
* Fixed a bug that causes schedule execution to fail intermittently

## Oct 29, 2024

### Release of a New Service
* Cloud Scheduler is a service that allows you set various tasks to run on a schedule of your choosing.