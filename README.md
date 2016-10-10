tinyagent
===============

Script for easy data collection of CPU, Memory, Disk, I/O Stats, Time Consistency, Load, Uptime, Network Interfaces and Network Statistics.

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
* 10/10/2016 - v4   - [FEATURE] Time Consistency
                      [FEATURE] Network Statistics.

Output
===============

Here's an output example:
```json
{
  "tinyagent": [
    {
      "hostname": "myserver01"
    },
    {
      "timestamp": 1476120558
    },
    {
      "netstatistics": {
        "IpExtInCEPkts": 0,
        "IpExtInECT0Pkts": 17,
        "IpExtInECT1Pkts": 0,
        "IpExtInNoECTPkts": 33754883,
        "IpExtInCsumErrors": 0,
        "IpExtOutBcastOctets": 18222670,
        "IpExtInBcastOctets": 631385883,
        "IpExtOutMcastOctets": 10048562,
        "IpExtInMcastOctets": 71990365,
        "IpExtOutOctets": 3530259872,
        "IpExtInOctets": 33868491458,
        "IpExtOutBcastPkts": 73522,
        "IpExtInBcastPkts": 3765481,
        "IpExtOutMcastPkts": 51138,
        "Icmp6OutTimeExcds": 0,
        "Icmp6OutPktTooBigs": 0,
        "Icmp6OutDestUnreachs": 0,
        "Icmp6InMLDv2Reports": 0,
        "Icmp6InRedirects": 0,
        "Icmp6InNeighborAdvertisements": 21,
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
        "Icmp6OutMsgs": 119,
        "Icmp6InErrors": 0,
        "Icmp6InMsgs": 21,
        "Ip6InCEPkts": 0,
        "Ip6InECT0Pkts": 0,
        "Ip6InECT1Pkts": 0,
        "Ip6InNoECTPkts": 18548,
        "Ip6OutBcastOctets": 0,
        "Ip6InBcastOctets": 0,
        "Ip6OutMcastOctets": 109251,
        "Ip6InMcastOctets": 7093806,
        "Ip6OutOctets": 102823,
        "Ip6InOctets": 7093946,
        "Ip6OutMcastPkts": 981,
        "Ip6InMcastPkts": 18546,
        "Ip6FragCreates": 0,
        "Ip6FragFails": 0,
        "Ip6FragOKs": 0,
        "Ip6ReasmFails": 0,
        "Ip6ReasmOKs": 0,
        "Ip6ReasmReqds": 0,
        "Ip6ReasmTimeout": 0,
        "Ip6OutNoRoutes": 420352,
        "Ip6OutDiscards": 4,
        "Ip6OutRequests": 910,
        "Ip6OutForwDatagrams": 0,
        "Ip6InDelivers": 18548,
        "Ip6InDiscards": 0,
        "Ip6InTruncatedPkts": 0,
        "Ip6InUnknownProtos": 0,
        "Ip6InAddrErrors": 0,
        "Ip6InNoRoutes": 0,
        "Ip6InTooBigErrors": 0,
        "Ip6InHdrErrors": 0,
        "Ip6InReceives": 18548,
        "UdpLiteInCsumErrors": 0,
        "UdpLiteSndbufErrors": 0,
        "UdpLiteRcvbufErrors": 0,
        "UdpLiteOutDatagrams": 0,
        "UdpLiteInErrors": 0,
        "UdpLiteNoPorts": 0,
        "UdpLiteInDatagrams": 0,
        "UdpInCsumErrors": 0,
        "UdpSndbufErrors": 0,
        "IcmpOutMsgs": 0,
        "IcmpInAddrMaskReps": 0,
        "IcmpInAddrMasks": 0,
        "IcmpInTimestampReps": 0,
        "IcmpInTimestamps": 79,
        "IcmpInEchoReps": 0,
        "IcmpInEchos": 0,
        "IcmpInRedirects": 0,
        "IcmpInSrcQuenchs": 0,
        "IcmpInParmProbs": 0,
        "IcmpInTimeExcds": 846,
        "IcmpInDestUnreachs": 0,
        "IcmpInCsumErrors": 19,
        "IcmpInErrors": 925,
        "IcmpInMsgs": 0,
        "IpFragCreates": 0,
        "IpOutRequests": 17199898,
        "IpInDelivers": 27084316,
        "IpInDiscards": 0,
        "IpInUnknownProtos": 0,
        "IpForwDatagrams": 0,
        "IpInAddrErrors": 0,
        "IpInHdrErrors": 0,
        "IpInReceives": 27296909,
        "IpOutDiscards": 4,
        "IpOutNoRoutes": 4,
        "IpReasmTimeout": 0,
        "IpReasmReqds": 0,
        "IpReasmOKs": 0,
        "IpReasmFails": 0,
        "IpFragOKs": 0,
        "IpFragFails": 0,
        "IcmpOutErrors": 31379,
        "IcmpOutDestUnreachs": 0,
        "IcmpOutTimeExcds": 31099,
        "IcmpOutParmProbs": 0,
        "IcmpOutSrcQuenchs": 0,
        "IcmpOutRedirects": 0,
        "IcmpOutEchos": 0,
        "IcmpOutEchoReps": 264,
        "IcmpOutTimestamps": 0,
        "IcmpOutTimestampReps": 0,
        "IcmpOutAddrMasks": 0,
        "IcmpOutAddrMaskReps": 0,
        "IcmpMsgInType0": 79,
        "IcmpMsgInType3": 846,
        "IcmpMsgOutType3": 31099,
        "IcmpMsgOutType8": 264,
        "IcmpMsgOutType69": 16,
        "TcpActiveOpens": 259665,
        "TcpPassiveOpens": 1,
        "TcpAttemptFails": 8316,
        "TcpEstabResets": 12934,
        "TcpInSegs": 9738091,
        "TcpOutSegs": 10067737,
        "TcpRetransSegs": 6069,
        "TcpInErrs": 1104,
        "TcpOutRsts": 28839,
        "TcpInCsumErrors": 0,
        "UdpInDatagrams": 18686774,
        "UdpNoPorts": 31320,
        "UdpInErrors": 175195,
        "UdpOutDatagrams": 7201209,
        "UdpRcvbufErrors": 33,
        "Icmp6OutParmProblems": 0,
        "Icmp6OutEchos": 0,
        "Icmp6OutEchoReplies": 0,
        "Icmp6OutGroupMembQueries": 0,
        "Icmp6OutGroupMembResponses": 0,
        "Icmp6OutGroupMembReductions": 0,
        "Icmp6OutRouterSolicits": 30,
        "Icmp6OutRouterAdvertisements": 0,
        "Icmp6OutNeighborSolicits": 16,
        "Icmp6OutNeighborAdvertisements": 0,
        "Icmp6OutRedirects": 0,
        "Icmp6OutMLDv2Reports": 73,
        "Icmp6InType136": 21,
        "Icmp6OutType133": 30,
        "Icmp6OutType135": 16,
        "Icmp6OutType143": 73,
        "Udp6InDatagrams": 36717,
        "Udp6NoPorts": 0,
        "Udp6InErrors": 0,
        "Udp6OutDatagrams": 785,
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
        "TcpExtSyncookiesFailed": 0,
        "TcpExtEmbryonicRsts": 0,
        "TcpExtPruneCalled": 4,
        "TcpExtRcvPruned": 0,
        "TcpExtOfoPruned": 0,
        "TcpExtOutOfWindowIcmps": 0,
        "TcpExtLockDroppedIcmps": 0,
        "TcpExtArpFilter": 0,
        "TcpExtTW": 43906,
        "TcpExtTWRecycled": 0,
        "TcpExtTWKilled": 0,
        "TcpExtPAWSPassive": 0,
        "TcpExtPAWSActive": 0,
        "TcpExtPAWSEstab": 7,
        "TcpExtDelayedACKs": 352676,
        "TcpExtDelayedACKLocked": 44,
        "TcpExtDelayedACKLost": 9630,
        "TcpExtListenOverflows": 0,
        "TcpExtListenDrops": 0,
        "TcpExtTCPPrequeued": 469,
        "TcpExtTCPDirectCopyFromBacklog": 666934,
        "TcpExtTCPDirectCopyFromPrequeue": 408123,
        "TcpExtTCPPrequeueDropped": 0,
        "TcpExtTCPHPHits": 5376152,
        "TcpExtTCPHPHitsToUser": 283,
        "TcpExtTCPPureAcks": 1543319,
        "TcpExtTCPHPAcks": 906016,
        "TcpExtTCPRenoRecovery": 0,
        "TcpExtTCPSackRecovery": 106,
        "TcpExtTCPSACKReneging": 0,
        "TcpExtTCPFACKReorder": 0,
        "TcpExtTCPSACKReorder": 0,
        "TcpExtTCPRenoReorder": 0,
        "TcpExtTCPTSReorder": 14,
        "TcpExtTCPFullUndo": 21,
        "TcpExtTCPPartialUndo": 8,
        "TcpExtTCPDSACKUndo": 5,
        "TcpExtTCPLossUndo": 367,
        "TcpExtTCPLostRetransmit": 0,
        "TcpExtTCPRenoFailures": 0,
        "TcpExtTCPSackFailures": 6,
        "TcpExtTCPLossFailures": 3,
        "TcpExtTCPFastRetrans": 135,
        "TcpExtTCPForwardRetrans": 23,
        "TcpExtTCPSlowStartRetrans": 3,
        "TcpExtTCPTimeouts": 1225,
        "TcpExtTCPLossProbes": 3020,
        "TcpExtTCPLossProbeRecovery": 1097,
        "TcpExtTCPRenoRecoveryFail": 0,
        "TcpExtTCPSackRecoveryFail": 0,
        "TcpExtTCPSchedulerFailed": 0,
        "TcpExtTCPRcvCollapsed": 247,
        "TcpExtTCPDSACKOldSent": 9479,
        "TcpExtTCPDSACKOfoSent": 268,
        "TcpExtTCPDSACKRecv": 1286,
        "TcpExtTCPDSACKOfoRecv": 0,
        "TcpExtTCPAbortOnData": 6119,
        "TcpExtTCPAbortOnClose": 7671,
        "TcpExtTCPAbortOnMemory": 0,
        "TcpExtTCPAbortOnTimeout": 741,
        "TcpExtTCPAbortOnLinger": 0,
        "TcpExtTCPAbortFailed": 0,
        "TcpExtTCPMemoryPressures": 0,
        "TcpExtTCPSACKDiscard": 0,
        "TcpExtTCPDSACKIgnoredOld": 0,
        "TcpExtTCPDSACKIgnoredNoUndo": 761,
        "TcpExtTCPSpuriousRTOs": 5,
        "TcpExtTCPMD5NotFound": 0,
        "TcpExtTCPMD5Unexpected": 0,
        "TcpExtTCPSackShifted": 0,
        "TcpExtTCPSackMerged": 105,
        "TcpExtTCPSackShiftFallback": 856,
        "TcpExtTCPBacklogDrop": 0,
        "TcpExtTCPMinTTLDrop": 0,
        "TcpExtTCPDeferAcceptDrop": 0,
        "TcpExtIPReversePathFilter": 0,
        "TcpExtTCPTimeWaitOverflow": 0,
        "TcpExtTCPReqQFullDoCookies": 0,
        "TcpExtTCPReqQFullDrop": 0,
        "TcpExtTCPRetransFail": 0,
        "TcpExtTCPRcvCoalesce": 1618556,
        "TcpExtTCPOFOQueue": 322625,
        "TcpExtTCPOFODrop": 0,
        "TcpExtTCPOFOMerge": 285,
        "TcpExtTCPChallengeACK": 1327,
        "TcpExtTCPSYNChallenge": 1104,
        "TcpExtTCPFastOpenActive": 0,
        "TcpExtTCPFastOpenPassive": 0,
        "TcpExtTCPFastOpenPassiveFail": 0,
        "TcpExtTCPFastOpenListenOverflow": 0,
        "TcpExtTCPFastOpenCookieReqd": 0,
        "TcpExtTCPSpuriousRtxHostQueues": 0,
        "TcpExtBusyPollRxPackets": 0,
        "IpExtInNoRoutes": 0,
        "IpExtInTruncatedPkts": 0,
        "IpExtInMcastPkts": 581479
      }
    },
    {
      "timeconsistency": [
        {
          "message": "server datetime OK",
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
          "rx_eth0": 75839
        },
        {
          "tx_eth0": 23771
        },
        {
          "rx_lo": 786
        },
        {
          "tx_lo": 786
        }
      ]
    },
    {
      "iostats": [
        {
          "sda1_time_spent_doing_io": 32,
          "sda1_time_spent_writing": 24,
          "sda1_time_spent_reading": 16,
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
              "used": 28668264
            },
            {
              "free": 18224632
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
          "memfree": 1578580
        },
        {
          "buffers": 95452
        },
        {
          "cached": 1063212
        }
      ]
    },
    {
      "cpuusage": [
        {
          "user": 19252934
        },
        {
          "system": 4978053
        },
        {
          "wait": 150975
        }
      ]
    },
    {
      "loadavg": [
        {
          "onemin": 0.2
        },
        {
          "fivemin": 0.15
        },
        {
          "tenmin": 0.2
        }
      ]
    },
    {
      "uptime": 1490468
    }
  ]
}
```
