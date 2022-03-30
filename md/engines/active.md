# ACTIVE ENGINE

## What is?

The Active Engine performs enumeration on target hostnames to determine active ones.

The Tool performs this enumeration using multiple techniques;
	--> DNS Lookup by resolving target to A(ipv4) or AAAA(ipv6) dns records as configured by user.
	--> Pinging the Target to see if its active.
	--> Trying to connect to target using different services e.g. HTTP, HTTPS, FTP, SSH etc. Rr any as specified by user.
	
This Tool uses multiple threads as alocated by the user to perform enumeration on targets also support use of multiple nameservers as provided
by the user or default list by s3s.


## Features 

1. Supports use of multiple nameservers.
2. Supports A(ipv4) and AAAA(ipv6) dns records lookups.
5. Supports multiple Targets lookup in one scan (one target after another).
5. Supports enumeration by connecting to host on specified ports eg (HTTP, HTTPS, FTP etc.).
6. Supports enumeration by Pinging The targets.

## Usage & Examples

<img src="images/active_1.png">

<img src="images/active_2.png">

Help improve the [documentation](https://github.com/3nock/s3s_doc)

## References


## NOTE:

*This is a very simple documentation on the Tool. It still doesn't contain many information on the many features of the tool & on how to effectively use the tool.*

*Help improve the [documentation](https://github.com/3nock/sub3suite_doc).*