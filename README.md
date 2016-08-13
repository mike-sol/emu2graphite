# emu2graphite
Daemon to send power demand stats from Rainforest Automation EMU-2 power meter to Graphite

Initial version is stupid simple and needs a ton of work. Serial port and Graphite server address are hardcoded.

TODO:
- Config file
- Better error handling
- Support for sending commands to EMU-2
- Power rate (cost) reading
- Improved resolution

Recommended Graphite storage config for this version:
[power]
pattern = ^power\.
retentions: 30s:7d,10m:90d,1h:1y
