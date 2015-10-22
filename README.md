# munin-plugin-GT784WN
Munin plugin for the ActionTec GT784WN ADSL Modem

## Requirements
  * Munin
  * Perl
  * Bundle::LWP

## Usage
  * ln -s .../modem_stats_ /usr/local/etc/munin/plugins/modem_stats_(hostname)_(reporttype)

### Reports supported:

  * snr
  * speed
  * uptime
  * retrains
  * crcerrors
  * wireless
  * lan
  * memory
  * sessions
