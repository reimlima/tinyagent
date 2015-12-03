tinyagent
===============

Script for easy data collection of CPU, Memory, Disk, Load and Uptime.

Output format: JSON

Notice
===============

This script was tested and work well in:

* Linux
        - OS Distribution: CentOS release 6.6 (Final)
        - Kernel: 2.6.32-504.3.3.el6.x86_64
        - GNU bash: version 4.1.2(1)-release (x86_64-redhat-linux-gnu)

Changelog
===============

- 30/04/2015    - v1    - First release.
- 04/05/2015    - v1.1  - Better "error description" to the log file.
- 03/12/2015    - v2    - Script now collect info from Network intarfaces. 

Output
===============

Here's an output example:

{
	"tinyagent": [{
		"hostname": "c019531"
	}, {
		"timestamp": 1449152309
	}, {
		"nettraffic": [{
			"rx_eth0": 148225
		}, {
			"tx_eth0": 19537
		}]
	}, {
		"diskusage": [{
			"mountpoint": "/",
			"usage": [{
				"total": 49426680
			}, {
				"used": 17541032
			}, {
				"free": 29351864
			}]
		}]
	}, {
		"memusage": [{
			"memtotal": 8131888
		}, {
			"memfree": 2104880
		}, {
			"buffers": 192028
		}, {
			"cached": 1742148
		}]
	}, {
		"cpuusage": [{
			"user": 458604
		}, {
			"system": 182236
		}, {
			"wait": 2806
		}]
	}, {
		"loadavg": [{
			"onemin": 0.46
		}, {
			"fivemin": 0.56
		}, {
			"tenmin": 0.58
		}]
	}, {
		"uptime": 13172
	}]
}
