# DNS ENGINE

## What is?

The DNS Engine resolves targets into specified DNS Records.
This Tool uses multiple threads as alocated by the user to perform enumeration on targets 
also support use of multiple nameservers as provided by the user or default list by s3s.

Records Supported by DNS Engine:

--> **A Records**: ipv4 address.
--> **AAAA Records**: ipv6 address.
--> **NS Records**: Nameservers records.
--> **MX Records**: Mail Exchange records.
--> **CNAME Records**: Canonical records.
--> **TXT Records**: TXT Records.
--> **SRV Records**: Service Records.

**NOTE:**

--> SOA and PTR DNS records are not supported for now.

## Features

1. Supports use of multiple nameservers.
2. Supports A(ipv4), AAAA(ipv6), NS, MX, TXT, CNAME and SRV dns records lookups.
3. Supports multiple Targets lookup in one scan.
4. SRV wordlist is also provided and can be modified as per user's liking

## Usage & Examples

<img src="images/dns_1.png">

<img src="images/dns_2.png">

Help improve the [documentation](https://github.com/3nock/s3s_doc)

## References


## NOTE:

*This is a very simple documentation on the Tool. It still doesn't contain many information on the many features of the tool & on how to effectively use the tool.*

*Help improve the [documentation](https://github.com/3nock/sub3suite_doc).*