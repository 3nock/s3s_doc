# ACTIVE ENGINE 

***Disclaimer 1:** This is a very simple documentation on the Tool. It still doesn't contain many information on the many features of the tool & on how to effectively use the tool. Help improve the [documentation](https://github.com/3nock/s3s_doc).*

***Disclaimer 2:** Incase of an unexpected error or erronous results please reach out by openning an [issue](https://github.com/3nock/sub3suite/issues) on the repo or on [Telegram](https://t.me/sub3suite) chat*.

## What is? 
The Active Engine performs enumeration on target hostnames to determine active ones.

The Tool performs this enumeration using multiple techniques;
	--> DNS Lookup by resolving target to A(ipv4) or AAAA(ipv6) dns records as configured by user.
	--> Pinging the Target to see if its active.
	--> Trying to connect to target using different services e.g. HTTP, HTTPS, FTP, SSH etc. Rr any as specified by user.
	
This Tool uses multiple threads as alocated by the user to perform enumeration on targets also support use of multiple nameservers as provided
by the user or default list by s3s.

You can obtain Passive Domains/Hostnames from the [OSINT Engine](../engines/osint.md) of Sub3 Suite

## Features 
1. Supports use of multiple nameservers.
2. Supports A(ipv4) and AAAA(ipv6) dns records lookups.
5. Supports multiple Targets lookup in one scan (one target after another).
5. Supports enumeration by connecting to host on specified ports eg (HTTP, HTTPS, FTP etc.).
6. Supports enumeration by Pinging The targets.

## Input Output: 

**Input:**Domain/Hostname

**Output:**Resolved Domain, IPv4,IPv6 & open Ports


## Scan Configuration values: 

<img src=images/active_config.png>

**Threads -** Number of threads to use for quering the targets. If number of threads is greater that the number of targets, then one thread per target will be used.

**Timeout -** Time for performing the lookup in milliseconds (terminates connection if timeout). It is advised for the timeout to be greater than 1000

**Record Type -** Record Type to lookup, A(IpV4), AAAA(IpV6), ANY(IpV4 and/or IpV6).

**No Duplicates -** Check to avoid duplicated results of the target

**AutoSave To Project -** Sends the obtained results directly to the project explorer as the scan progresses

<img src=images/brute_nameservers.png>

**Nameservers -** - Nameservers to use for DNS lookup. You can choose; 

***single nameserver:*** by checking the single nameserver radio-button and choose the nameserver in the combo-box

***random nameserver:*** by checking the random nameserver radio-button and Sub3 Suite will use its default set of nameservers, assigning them randomly

***custom nameserver:*** by checking the random nameserver radio-button and enter the ip addresses of the nameservers you want to use

## Usage & Examples

1. Choose the **output(scan type)** first. **active DNS:** Resolves DNS records for target(s) and **Active PORT:** Port scans The Target(s)

<img src=images/active_output.png>

3. Enter Target/Targets:

	a. for **single target** just enter the targets on the lineEdit.
	
	<img src=images/active_target.png>
	
	b. For **multiple targets**; check the **Multiple Targets** checkbox, add your targets to the listView.
	
	<img src=images/active_targets.png>
	
4. For port scan. input the ports, **Default:** scans for common ports, **Range:** scans for a range of ports, **Custom:** Scans for a port or list ports

<img src=images/active_ports.png>

5. **Start** scan. You can **Pause, Resume** and **Stop** the scan.

6. You can also **Re-Scan** failed scans(scans that returned an error) with different configurations.

<img src=images/brute_rescan.png>

7. Several ***Actions*** can be performed on the obtained results.

## Actions: 

Details on the actions for the obtained results.

<img src=images/active_actions.png>

 - The Actions on Results are accessible via the **Actions >** button and **Right-Click** on the Results. & are only active when the results are present

1. **Clear:**Clears the results and the progress bar.
2. **Expand & Collapse:**Expands the all areas of the result tree and Collapse all areas of the result tree respectively
3. **Save:**Saves the obtained Results To a File. Saves in Json format
4. **Copy:**Copies the results on the clipboard. Copies in Json format
5. **Send To Project:**Sends the Obtained results to the project explorer.
5. **Send * To *:**Sends the Result Type to the choosen Engine/Enumerator.

**NOTE: **
	If you have filtered the results using the filter. the above actions will only be performed on the remaing results after filter