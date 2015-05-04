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

Output
===============

Here's an output example:

	{
		"tinyagent": [
			{
				"hostname": "localserver"
			},
			{
				"timestamp": 1234567890
			},
			{
				"diskusage": [
					{
						"mountpoint": "/",
						"usage": [
							{
								"total": 49426680
							},
							{
								"used": 20333656
							},
							{
								"free": 26559240
							}
						]
					}
				]
			},
			{
				"memusage": [
					{
						"memtotal": 8053536
					},
					{
						"memfree": 416368
					},
					{
						"buffers": 140320
					},
					{
						"cached": 1829176
					}
				]
			},
			{
				"cpuusage": [
					{
						"user": 9876218
					},
					{
						"system": 3015700
					},
					{
						"wait": 87097
					}
				]
			},
			{
				"loadavg": [
					{
						"onemin": 0.2
					},
					{
						"fivemin": 0.21
					},
					{
						"tenmin": 0.16
					}
				]
			},
			{
				"uptime": 1060048
			}
		]
	}
