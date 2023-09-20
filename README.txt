=====================
MIDPEM Update Manager
=====================

This program allows for interface with a MIDPEM-managed program enabling easy
remote update deployment and rollback on distributed and multi-process systems.

Place all initial code in the "program" directory, or choose to leave blank and
install an initial update remotely.  An "id.txt" file must, however, be present
within this "program" directory initially and at all times.  This file
identifies the MIDPEM system and cannot be changed remotely.

When performing an update, all new and modified files must be placed directly
within a zipfile and sent to the update management bot with an appropriate
command.  The update manager does not delete files that are not included in
the update deployment zipfile, but rather performs a merge.  Any new files or
directories from the deployment zipfile are added to the current "program"
directory, and any existing files are updated.

=========
Commands:
=========

$update <device_id>
-------------------
alias: $up
brief: used to deploy an update zipfile to remote connected bot with given ID

$updateall
----------
alias: $upa
brief: used to deploy an update zipfile to all remote connected bots

$rollback <device_id>
---------------------
alias: $rb
brief: used to initiate a rolback on remote connected bot with given ID

$rolbackall
-----------
alias: $rba
brief: used to initiate a rolback on all remote connected bots

$status
-------
alias: $ss
brief: used to ping bot with given ID (or all bots)

$statusall
----------
alias: $ssa
brief: used to ping all connected bots