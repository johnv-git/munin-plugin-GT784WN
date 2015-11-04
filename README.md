# munin-plugin-GT784WN
Munin plugin for the ActionTec GT784WN ADSL Modem.

## Requirements
  * Munin
  * Perl
  * Bundle::LWP

## Usage
  * ln -s .../modem_stats_ /usr/local/etc/munin/plugins/modem_stats_(hostname)_(reporttype)

### Reports supported:
  * snr 
    * Down SNR 
    * Up SNR
    * Down Attenuation
    * Up Attenuation
    * Down Power
    * Up Power
  * speed 
    * Down Speed
    * Up Speed
  * uptime
    * days
  * retrains
    * count
  * crcerrors
    * Near CRC
    * Far CRC
    * Near FEC
    * Far FEC
  * wireless
    * Recv PPS
    * Send PPS
  * lan
    * Recv PPS
    * Send PPS
  * memory
    * % Used
  * sessions
    * Total
    * TCP
    * UDP
    * Modem

### Interpreting Charts:
In general, this is useful to detect line degradation over time.  Perhaps the copper to your house does poorly in the
rain.  Perhaps your dsl is unstable after the neighbor had their phone installed.  Perhaps you lose sync every night
because someone turns on a massive RF-generating dimmer switch.


#### Firmware Issues:
The GT784WN firmware (*NCS01-1.0.13*) has a number of issues.

  * Down Power always reports 0.
  * Network I/O in packets per second, not bytes.
  * Session use seemingly reports incorrectly.
