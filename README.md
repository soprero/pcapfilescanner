# pcapfilescanner

This program processes network packet capture files (pcap) you created by running a
network packet capture program (e.g. wireshark, tcpdump) and extracts statistics.

This program is an x64 Windows 10 program.  A command line version will be released
at a later time.

Process:
  1. You choose one or more capture files.
  1. You start the processing.
  1. The program does the processing which can take a while, depending
     on the number and sizes of the input files. You can expect a processing
     speed of up to 100 MB/s, depending on the mass storage the input files
     are stored at.
  1. You can browse the various statistical numbers in the UI and export
     some of them in CSV format to the clipboard for further processing
     (e.g. paste into Excel).

This program is currently work in progress and in an alpha state.

Supports packet capture files in classic (pcap) and new (pcapng) file formats.

The current alpha version supports the following statistical numbers:
    
* Layer 2
    * General Ethernet Statistics
    * MAC/Ethernet Addresses:
      * Source addresses, Destination addresses, Multi-/Broadcast addresses
    * Ethernet frame size histogram
    * Linux Cooked Mode Statistics
    * Linux Cooked Mode frame size histogram
    * ARP: Packet counts
    * ARP: Extracted address mappings
    * IPv4: General Statistics
    * IPv4: Address lists
        * Source addresses, Dest addresses, Source+Dest addresses,
            Source only addresses, Dest only addresses
        * each address with timestamps: first seen, last seen
        * lists can be filtered by address ranges
    * TCP:
        * Source and Dest ports used
    * DNS:
        * General Statistics
        * Queried Names (A record: IPv4)
        * Resolved Names (A record: IPv4)
        * Unresolved Names (A record)
        * Record Type counters
        * LOC records
    * DHCP:
        * Client MAC addresses
        * Host names
    * HTTP (not HTTPS)
        * Request Targets (URLs)
        * Request User Agents
        * Response Status Codes
        * Server Software (extracted from Responses)
        * Content Types


Changes for version 2020-09-17 (first version on github):
    
  * Added Popup menu system.
  * Layer 2: added extraction of VLAN IDs.
  * DNS: added counters of record types.
  * DNS: added extraction of LOC records.
  * DHCP: added extraction of client MAC addresses and host names.

