# BRUTE ENGINE

## What is?

The BRUTE Engine performs subdomain & TLD enumeration by bruteforce.
Performs DNS lookup on subdomain & TLD created by appending the words from wordlist to the
target.
The tool accomplishes this by resolving the targets using the public nameservers or internal nameservers as provided
by the user.
The domains are resolved to either A(ipv4) or AAAA(ipv6) dns records depending on the scan configuration by user.
The resolved subdomains or TLDs does not necessarily mean the targets are active but an indicator that they can be resolved by
the particular nameservers.

This Tool uses multiple threads as alocated by the user to perform DNS lookup on targets also support use of multiple nameservers as provided
by the user or default list by s3s.


## Features

1. Supports use of multiple nameservers.
2. Supports A(ipv4) and AAAA(ipv6) dns records lookups.
3. Supports subdomain(e.g. *.example.com) and Top-level-domain(TLD e.g. example.*) bruteforcing.
4. Supports automated multi-level scan (*.example.com --> *.*.example.com --> *.*.*.example.com).
5. Supports multiple Targets lookup in one scan (one target after another).
5. Has a simple wordlist generator(still an early feature, will be advanced later).

## Usage & Examples

<img src="images/brute_1.png">

<img src="images/brute_2.png">

Help improve the [documentation](https://github.com/3nock/s3s_doc)

## References


## NOTE:

*This is a very simple documentation on the Tool. It still doesn't contain many information on the many features of the tool & on how to effectively use the tool.*

*Help improve the [documentation](https://github.com/3nock/sub3suite_doc).*