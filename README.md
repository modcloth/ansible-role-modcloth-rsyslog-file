Role Name
========

This role uses the imfile rsyslog module and writes a configuration file for rsyslog to watch given log files.

Requirements
------------

Rsyslogd should already be installed.

Role Variables
--------------

`location`: The location to write the rsyslog config file (defaults to `/etc/rsyslog.d`)
`service`: The name of the service (gets used to generate the rsyslog configuration file name)
`files`: array of `file` (hash)
`file`:
- `name`: The name of the file to watch
- `state_file`: Used for $InputFileStateFile (defaults to the basename)
- `tag`: Used for $InputFileTag (defaults to service)
- `severity`: Used for $InputFileSeverity (defaults to notice)

License
-------

MIT

Author Information
------------------

Jesse Szwedko

ModCloth Inc.
