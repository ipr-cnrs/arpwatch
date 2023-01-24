## v2.0.1

### Fix
* Use flatten to manage packages list.

## v2.0.0

### Features
* Adapt for Debian Buster (starts with Arpwatch version 2.1a15-7).
* Drop Debian Stretch support. Stay in v1.* to be able to manage Arpwatch on Debian Stretch.

### Fix
* Arpwatch doesn't support configuration file. Remove /etc/arpwatch.conf

## v1.0.2

### Fix
* Fix E405 Remote package tasks should have a retry.
* Fix E102 No Jinja2 in when.
* Fix E404 Doesn't need a relative path in role.

## v1.0.1

### Fix
* Set empty dependencies line to fix Galaxy warning.
* Use to_nice_json to manage packages list.

## v1.0.0

### Features
* Install Arpwatch.
* Ensure the service is in the desired state.
* Allow to set the user that run Arpwatch.
* Allow to set arguments to pass Arpwatch service.
