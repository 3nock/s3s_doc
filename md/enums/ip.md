# IP Enumerator 

***Disclaimer 1:** This is a very simple documentation on the Tool. It still doesn't contain many information on the many features of the tool & on how to effectively use the tool. Help improve the [documentation](https://github.com/3nock/s3s_doc).*

***Disclaimer 2:** Incase of an unexpected error or erronous results please reach out by openning an [issue](https://github.com/3nock/sub3suite/issues) on the repo or on [Telegram](https://t.me/sub3suite) chat*.

## What is? 

**IP Address -** An Internet Protocol address (IP address) is a numerical label such as 192.0.2.1 that is connected to a computer network that uses the Internet Protocol for communication.[1][2] An IP address serves two main functions: network interface identification and location addressing.
Internet Protocol version 4 (IPv4) defines an IP address as a 32-bit number.[2] However, because of the growth of the Internet and the depletion of available IPv4 addresses, a new version of IP (IPv6), using 128 bits for the IP address, was standardized in 1998.
[reference](https://en.wikipedia.org/wiki/IP_address).

You can obtain IP from the [OSINT Engine](../engines/osint.md), [BRUTE Engine](../engines/brute.md) and [ACTIVE Engine](../engines/active.md) of Sub3 Suite

**IP Enumerator -** Is Used to return list useful information about the IP. 
sub3suite's IP Enumerator queries this data from OSINT sources that provide Reverse IP Info lookup.

## Input Output 

**Input:** IP Address
**Output:** IP Address Info: owner's address, location, company, ASN, privacy info and Route

## Features: 

**Multiple Targets search:** Search mulitple targets and the enumerator will provide the results for every targets.


## Scan Configuration values: 

**Timeout -** Time for performing the lookup in milliseconds (terminates connection if timeout). It is advised for the timeout to be greater than 1000
**No Duplicates -** Check to avoid duplicated results of the target
**AutoSave To Project -** Sends the obtained results directly to the project explorer as the scan progresses


## Usage: 

1. Set the scan configuration by clicking the **config** button, setting the values and save.
2. **If single Target:** enter target (IP) on the LineEdit. **If multiple Targets:** check the **Multile Targes** checkbox and enter the target values (IP) on the ListView marked by **Targets**. 
3. Start The scan

## Actions: 

Details on the actions for the obtained results.

 - The Actions on Results are accessible via the **Actions >** button and **Right-Click** on the Results. & are only active when the results are present

1. **Clear:** Clears the results and the progress bar.
2. **Expand & Collapse:** Expands the all areas of the result tree and Collapse all areas of the result tree respectively
3. **Save:** Saves the obtained Results To a File. Saves in Json format
4. **Copy:** Copies the results on the clipboard. Copies in Json format
5. **Send To Project:** Sends the Obtained results to the project explorer.

**NOTE:**
	If you have filtered the results using the filter. the above actions will only be performed on the remaing results after filter
	
## References: 
1. [what is an ip address](https://www.kaspersky.com/resource-center/definitions/what-is-an-ip-address)