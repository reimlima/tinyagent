tinyagent
===============

Script for easy data collection of CPU, Memory, Disk, Load, Uptime and Network Interfaces.

Output format: JSON

Notice
===============

This script was tested and work well in:

* System: Linux
* OS Distribution: CentOS release 6.6 (Final)
* Kernel: 2.6.32-504.3.3.el6.x86_64
* GNU bash: version 4.1.2(1)-release (x86_64-redhat-linux-gnu)

Changelog
===============

* 30/04/2015 - v1   - First release.
* 04/05/2015 - v1.1 - [FIX] Better "error description" to the log file.
* 03/12/2015 - v2   - [FEATURE] Script now collect info from Network intarfaces. 
* 14/04/2016 - v2.1 - [FIX] Fix 'Network intarfaces' json format.
                      [FIX] Better output in 'df' command.
* 07/10/2016 - v3   - [FIX] Now it show all 'Network intarfaces' no matter the name.
                      [FEATURE] I/O read and write informations for all partitions.

Output
===============

Here's an output example:
```json
{
  "tinyagent": [
    {
      "hostname": "c019531"
    },
    {
      "timestamp": 1475852706
    },
    {
      "nettraffic": [
        {
          "rx_docker0": 0
        },
        {
          "tx_docker0": 0
        },
        {
          "rx_eth0": 83828
        },
        {
          "tx_eth0": 10510
        },
        {
          "rx_eth1": 0
        },
        {
          "tx_eth1": 0
        },
        {
          "rx_lo": 0
        },
        {
          "tx_lo": 0
        }
      ]
    },
    {
      "iostats": [
        {
          "sda1_time_spent_doing_io": 16,
          "sda1_time_spent_writing": 12,
          "sda1_time_spent_reading": 4,
          "partition": "sda1"
        },
        {
          "sda2_time_spent_doing_io": 0,
          "sda2_time_spent_writing": 0,
          "sda2_time_spent_reading": 0,
          "partition": "sda2"
        },
        {
          "sda5_time_spent_doing_io": 0,
          "sda5_time_spent_writing": 0,
          "sda5_time_spent_reading": 0,
          "partition": "sda5"
        },
        {
          "sdb1_time_spent_doing_io": 0,
          "sdb1_time_spent_writing": 0,
          "sdb1_time_spent_reading": 0,
          "partition": "sdb1"
        },
        {
          "sdb2_time_spent_doing_io": 0,
          "sdb2_time_spent_writing": 0,
          "sdb2_time_spent_reading": 0,
          "partition": "sdb2"
        },
        {
          "sr0_time_spent_doing_io": 0,
          "sr0_time_spent_writing": 0,
          "sr0_time_spent_reading": 0,
          "partition": "sr0"
        }
      ]
    },
    {
      "diskusage": [
        {
          "usage": [
            {
              "total": 49426680
            },
            {
              "used": 28709620
            },
            {
              "free": 18183276
            }
          ],
          "mountpoint": "/"
        }
      ]
    },
    {
      "memusage": [
        {
          "memtotal": 8131864
        },
        {
          "memfree": 1429992
        },
        {
          "buffers": 285272
        },
        {
          "cached": 1512820
        }
      ]
    },
    {
      "cpuusage": [
        {
          "user": 17545588
        },
        {
          "system": 4562472
        },
        {
          "wait": 132386
        }
      ]
    },
    {
      "loadavg": [
        {
          "onemin": 0.3
        },
        {
          "fivemin": 0.35
        },
        {
          "tenmin": 0.32
        }
      ]
    },
    {
      "uptime": 1222635
    }
  ]
}

```
