# tinyagent

Script for easy data collection of:
* CPU
* Memory
* Disk
* I/O Stats
* Time Consistency
* Load
* Uptime
* A list of Process
* Network Interfaces
* Network Statistics

Output format: JSON

### Notice

This script was tested and work well in:

* System: Linux
* OS Distribution: CentOS release 6.6 (Final)
* Kernel: 2.6.32-504.3.3.el6.x86_64
* GNU bash: version 4.1.2(1)-release (x86_64-redhat-linux-gnu)

### Changelog

* 30/04/2015 - v1   - First release.
* 04/05/2015 - v1.1 - [FIX] Better "error description" to the log file.
* 03/12/2015 - v2   - [FEATURE] Script now collect info from Network intarfaces. 
* 14/04/2016 - v2.1 - [FIX] Fix 'Network intarfaces' json format.
                      [FIX] Better output in 'df' command.
* 07/10/2016 - v3   - [FIX] Now it show all 'Network intarfaces' no matter the name.
                      [FEATURE] I/O read and write informations for all partitions.
* 10/10/2016 - v4   - [FEATURE] Time Consistency
                      [FEATURE] Network Statistics.
* 25/10/2016 - v5   - [FEATURE] Monitoring a Process List.


### Monitoring a Process List

This option allow the script to monitoring a list of processes which are listening to a TCP port.

Just insert the list of ports in "PROCESSPORTARRAY" inside the script, like the example below:

```sh
PROCESSPORTARRAY=("443" "22")
```

### Output

Here's an output example:
```json
{
  "tinyagent": [
    {
      "hostname": "c019531"
    },
    {
      "timestamp": 1477423244
    },
    {
      "processmonitoring": [
        {
          "process_count_443": "0",
          "process_443": "down"
        },
        {
          "process_count_22": "9",
          "process_22": "up"
        }
      ]
    },
    {
      "netstatistics": {
        "IpExtInCEPkts": 0,
        "IpExtInECT0Pkts": 358,
        "IpExtInECT1Pkts": 0,
        "IpExtInNoECTPkts": 14176814,
        "IpExtInCsumErrors": 0,
        "IpExtOutBcastOctets": 7936961,
        "IpExtInBcastOctets": 225395405,
        "IpExtOutMcastOctets": 4203568,
        "IpExtInMcastOctets": 31315789,
        "IpExtOutOctets": 1175998399,
        "IpExtInOctets": 14470348760,
        "IpExtOutBcastPkts": 34638,
        "IpExtInBcastPkts": 1527065,
        "IpExtOutMcastPkts": 21388,
        "IpExtInMcastPkts": 264335,
        "Icmp6OutPktTooBigs": 0,
        "Icmp6OutDestUnreachs": 0,
        "Icmp6InMLDv2Reports": 0,
        "Icmp6InRedirects": 0,
        "Icmp6InNeighborAdvertisements": 13,
        "Icmp6InNeighborSolicits": 0,
        "Icmp6InRouterAdvertisements": 0,
        "Icmp6InRouterSolicits": 0,
        "Icmp6InGroupMembReductions": 0,
        "Icmp6InGroupMembResponses": 0,
        "Icmp6InGroupMembQueries": 0,
        "Icmp6InEchoReplies": 0,
        "Icmp6InEchos": 0,
        "Icmp6InParmProblems": 0,
        "Icmp6InTimeExcds": 0,
        "Icmp6InPktTooBigs": 0,
        "Icmp6InDestUnreachs": 0,
        "Icmp6InCsumErrors": 0,
        "Icmp6OutErrors": 0,
        "Icmp6OutMsgs": 10,
        "Icmp6InErrors": 0,
        "Icmp6InMsgs": 13,
        "Ip6InCEPkts": 0,
        "Ip6InECT0Pkts": 0,
        "Ip6InECT1Pkts": 0,
        "Ip6InNoECTPkts": 18446,
        "Ip6OutBcastOctets": 0,
        "Ip6InBcastOctets": 0,
        "Ip6OutMcastOctets": 26111,
        "Ip6InMcastOctets": 5133407,
        "Ip6OutOctets": 277914,
        "Ip6InOctets": 5385686,
        "Ip6OutMcastPkts": 255,
        "Ip6InMcastPkts": 17742,
        "Ip6FragCreates": 0,
        "Ip6FragFails": 0,
        "Ip6FragOKs": 0,
        "Ip6ReasmFails": 0,
        "Ip6ReasmOKs": 0,
        "Ip6ReasmReqds": 0,
        "Ip6ReasmTimeout": 0,
        "Ip6OutNoRoutes": 213900,
        "Ip6OutDiscards": 0,
        "Ip6OutRequests": 953,
        "Ip6OutForwDatagrams": 0,
        "Ip6InDelivers": 18446,
        "Ip6InDiscards": 0,
        "Ip6InTruncatedPkts": 0,
        "Ip6InUnknownProtos": 0,
        "Ip6InAddrErrors": 0,
        "Ip6InNoRoutes": 0,
        "Ip6InTooBigErrors": 0,
        "Ip6InHdrErrors": 0,
        "Ip6InReceives": 18446,
        "UdpLiteInCsumErrors": 0,
        "UdpLiteSndbufErrors": 0,
        "UdpLiteRcvbufErrors": 0,
        "UdpLiteOutDatagrams": 0,
        "UdpLiteInErrors": 0,
        "UdpLiteNoPorts": 0,
        "UdpLiteInDatagrams": 0,
        "UdpInCsumErrors": 0,
        "UdpSndbufErrors": 0,
        "UdpRcvbufErrors": 0,
        "IcmpOutMsgs": 0,
        "IcmpInAddrMaskReps": 0,
        "IcmpInAddrMasks": 0,
        "IcmpInTimestampReps": 0,
        "IcmpInTimestamps": 89,
        "IcmpInEchoReps": 0,
        "IcmpInEchos": 0,
        "IcmpInRedirects": 0,
        "IcmpInSrcQuenchs": 0,
        "IcmpInParmProbs": 246,
        "IcmpInTimeExcds": 902,
        "IcmpInDestUnreachs": 0,
        "IcmpInCsumErrors": 123,
        "IcmpInErrors": 1237,
        "IcmpInMsgs": 0,
        "IpFragCreates": 0,
        "IpOutRequests": 7025430,
        "IpInDelivers": 11437894,
        "IpInDiscards": 0,
        "IpInUnknownProtos": 0,
        "IpForwDatagrams": 0,
        "IpInAddrErrors": 0,
        "IpInHdrErrors": 0,
        "IpInReceives": 11532480,
        "IpOutDiscards": 60,
        "IpOutNoRoutes": 6,
        "IpReasmTimeout": 0,
        "IpReasmReqds": 0,
        "IpReasmOKs": 0,
        "IpReasmFails": 0,
        "IpFragOKs": 0,
        "IpFragFails": 0,
        "IcmpOutErrors": 13678,
        "IcmpOutDestUnreachs": 0,
        "IcmpOutTimeExcds": 13043,
        "IcmpOutParmProbs": 0,
        "IcmpOutSrcQuenchs": 0,
        "IcmpOutRedirects": 0,
        "IcmpOutEchos": 0,
        "IcmpOutEchoReps": 221,
        "IcmpOutTimestamps": 0,
        "IcmpOutTimestampReps": 0,
        "IcmpOutAddrMasks": 0,
        "IcmpOutAddrMaskReps": 0,
        "IcmpMsgInType0": 89,
        "IcmpMsgInType3": 902,
        "IcmpMsgInType11": 246,
        "IcmpMsgOutType3": 13043,
        "IcmpMsgOutType8": 221,
        "IcmpMsgOutType69": 414,
        "TcpActiveOpens": 104890,
        "TcpPassiveOpens": 83,
        "TcpAttemptFails": 434,
        "TcpEstabResets": 4193,
        "TcpInSegs": 3963484,
        "TcpOutSegs": 3920392,
        "TcpRetransSegs": 3568,
        "TcpInErrs": 640,
        "TcpOutRsts": 13400,
        "TcpInCsumErrors": 3,
        "UdpInDatagrams": 8143558,
        "UdpNoPorts": 13077,
        "UdpInErrors": 40159,
        "UdpOutDatagrams": 3159658,
        "Icmp6OutTimeExcds": 0,
        "Icmp6OutParmProblems": 0,
        "Icmp6OutEchos": 0,
        "Icmp6OutEchoReplies": 0,
        "Icmp6OutGroupMembQueries": 0,
        "Icmp6OutGroupMembResponses": 0,
        "Icmp6OutGroupMembReductions": 0,
        "Icmp6OutRouterSolicits": 3,
        "Icmp6OutRouterAdvertisements": 0,
        "Icmp6OutNeighborSolicits": 1,
        "Icmp6OutNeighborAdvertisements": 0,
        "Icmp6OutRedirects": 0,
        "Icmp6OutMLDv2Reports": 6,
        "Icmp6InType136": 13,
        "Icmp6OutType133": 3,
        "Icmp6OutType135": 1,
        "Icmp6OutType143": 6,
        "Udp6InDatagrams": 35029,
        "Udp6NoPorts": 0,
        "Udp6InErrors": 0,
        "Udp6OutDatagrams": 239,
        "Udp6RcvbufErrors": 0,
        "Udp6SndbufErrors": 0,
        "Udp6InCsumErrors": 0,
        "UdpLite6InDatagrams": 0,
        "UdpLite6NoPorts": 0,
        "UdpLite6InErrors": 0,
        "UdpLite6OutDatagrams": 0,
        "UdpLite6RcvbufErrors": 0,
        "UdpLite6SndbufErrors": 0,
        "UdpLite6InCsumErrors": 0,
        "TcpExtSyncookiesSent": 0,
        "TcpExtSyncookiesRecv": 0,
        "TcpExtSyncookiesFailed": 5,
        "TcpExtEmbryonicRsts": 0,
        "TcpExtPruneCalled": 0,
        "TcpExtRcvPruned": 0,
        "TcpExtOfoPruned": 0,
        "TcpExtOutOfWindowIcmps": 0,
        "TcpExtLockDroppedIcmps": 0,
        "TcpExtArpFilter": 0,
        "TcpExtTW": 16368,
        "TcpExtTWRecycled": 0,
        "TcpExtTWKilled": 0,
        "TcpExtPAWSPassive": 0,
        "TcpExtPAWSActive": 0,
        "TcpExtPAWSEstab": 11,
        "TcpExtDelayedACKs": 151114,
        "TcpExtDelayedACKLocked": 23,
        "TcpExtDelayedACKLost": 3744,
        "TcpExtListenOverflows": 0,
        "TcpExtListenDrops": 0,
        "TcpExtTCPPrequeued": 1150,
        "TcpExtTCPDirectCopyFromBacklog": 89215,
        "TcpExtTCPDirectCopyFromPrequeue": 1924414,
        "TcpExtTCPPrequeueDropped": 0,
        "TcpExtTCPHPHits": 2148330,
        "TcpExtTCPHPHitsToUser": 837,
        "TcpExtTCPPureAcks": 629238,
        "TcpExtTCPHPAcks": 348850,
        "TcpExtTCPRenoRecovery": 0,
        "TcpExtTCPSackRecovery": 14,
        "TcpExtTCPSACKReneging": 0,
        "TcpExtTCPFACKReorder": 0,
        "TcpExtTCPSACKReorder": 0,
        "TcpExtTCPRenoReorder": 0,
        "TcpExtTCPTSReorder": 1,
        "TcpExtTCPFullUndo": 2,
        "TcpExtTCPPartialUndo": 1,
        "TcpExtTCPDSACKUndo": 0,
        "TcpExtTCPLossUndo": 155,
        "TcpExtTCPLostRetransmit": 0,
        "TcpExtTCPRenoFailures": 0,
        "TcpExtTCPSackFailures": 4,
        "TcpExtTCPLossFailures": 0,
        "TcpExtTCPFastRetrans": 16,
        "TcpExtTCPForwardRetrans": 0,
        "TcpExtTCPSlowStartRetrans": 0,
        "TcpExtTCPTimeouts": 790,
        "TcpExtTCPLossProbes": 1926,
        "TcpExtTCPLossProbeRecovery": 978,
        "TcpExtTCPRenoRecoveryFail": 0,
        "TcpExtTCPSackRecoveryFail": 0,
        "TcpExtTCPSchedulerFailed": 0,
        "TcpExtTCPRcvCollapsed": 0,
        "TcpExtTCPDSACKOldSent": 3250,
        "TcpExtTCPDSACKOfoSent": 376,
        "TcpExtTCPDSACKRecv": 1134,
        "TcpExtTCPDSACKOfoRecv": 0,
        "TcpExtTCPAbortOnData": 2471,
        "TcpExtTCPAbortOnClose": 2930,
        "TcpExtTCPAbortOnMemory": 0,
        "TcpExtTCPAbortOnTimeout": 381,
        "TcpExtTCPAbortOnLinger": 0,
        "TcpExtTCPAbortFailed": 0,
        "TcpExtTCPMemoryPressures": 0,
        "TcpExtTCPSACKDiscard": 0,
        "TcpExtTCPDSACKIgnoredOld": 0,
        "TcpExtTCPDSACKIgnoredNoUndo": 931,
        "TcpExtTCPSpuriousRTOs": 7,
        "TcpExtTCPMD5NotFound": 0,
        "TcpExtTCPMD5Unexpected": 0,
        "TcpExtTCPSackShifted": 0,
        "TcpExtTCPSackMerged": 5,
        "TcpExtTCPSackShiftFallback": 289,
        "TcpExtTCPBacklogDrop": 0,
        "TcpExtTCPMinTTLDrop": 0,
        "TcpExtTCPDeferAcceptDrop": 0,
        "TcpExtIPReversePathFilter": 0,
        "TcpExtTCPTimeWaitOverflow": 0,
        "TcpExtTCPReqQFullDoCookies": 0,
        "TcpExtTCPReqQFullDrop": 0,
        "TcpExtTCPRetransFail": 0,
        "TcpExtTCPRcvCoalesce": 700095,
        "TcpExtTCPOFOQueue": 119810,
        "TcpExtTCPOFODrop": 0,
        "TcpExtTCPOFOMerge": 429,
        "TcpExtTCPChallengeACK": 647,
        "TcpExtTCPSYNChallenge": 637,
        "TcpExtTCPFastOpenActive": 0,
        "TcpExtTCPFastOpenPassive": 0,
        "TcpExtTCPFastOpenPassiveFail": 0,
        "TcpExtTCPFastOpenListenOverflow": 0,
        "TcpExtTCPFastOpenCookieReqd": 0,
        "TcpExtTCPSpuriousRtxHostQueues": 1,
        "TcpExtBusyPollRxPackets": 0,
        "IpExtInNoRoutes": 0,
        "IpExtInTruncatedPkts": 0
      }
    },
    {
      "timeconsistency": [
        {
          "message": "server datetime ok",
          "status": 0
        }
      ]
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
          "rx_eth0": 56044800
        },
        {
          "tx_eth0": 1986003
        },
        {
          "rx_lo": 7676
        },
        {
          "tx_lo": 7676
        }
      ]
    },
    {
      "iostats": [
        {
          "sda1_time_spent_doing_io": 948,
          "sda1_time_spent_writing": 16584,
          "sda1_time_spent_reading": 24,
          "partition": "sda1"
        },
        {
          "sda2_time_spent_doing_io": 0,
          "sda2_time_spent_writing": 0,
          "sda2_time_spent_reading": 0,
          "partition": "sda2"
        },
        {
          "sda5_time_spent_doing_io": 8,
          "sda5_time_spent_writing": 12,
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
              "used": 29235484
            },
            {
              "free": 17657412
            }
          ],
          "mountpoint": "/"
        }
      ]
    },
    {
      "memusage": [
        {
          "memtotal": 8131860
        },
        {
          "memfree": 288060
        },
        {
          "buffers": 223652
        },
        {
          "cached": 2220164
        }
      ]
    },
    {
      "cpuusage": [
        {
          "user": 8234942
        },
        {
          "system": 2317372
        },
        {
          "wait": 61528
        }
      ]
    },
    {
      "loadavg": [
        {
          "onemin": 1.25
        },
        {
          "fivemin": 1.36
        },
        {
          "tenmin": 1.19
        }
      ]
    },
    {
      "uptime": 627524
    }
  ]
}
```
