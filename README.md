# megaraid-scripts
MegaRAID controller scripts for monitoring and diagnostics.

These scripts require the appropriat MegaRAID utility to be installed:
* storcli - most vendors, including IBM/Lenovo
* perccli - Dell PERC branded controllers

## megaraid-checkup

Script for checking for MegaRAID controllers for problems.

Errors are emitted for items with non-OK status, ie broken drives, cache modules etc.

Warnings are emitted when unrecoverable media errors are detected, rebuilds are in progress, attached drives are unused, and more.

If no errors or warnings are detected, the script gives no output making it ideal to use as a daily check in a cron job (no news is good news).

###

`megaraid-checkup` - Checks all Smart Array controllers for issues

`env DEBUG=1 megaraid-checkup` - Same as above, but also prints informational messages about detected devices.
