# CIDR Enumerator 

***Disclaimer 1:** This is a very simple documentation on the Tool. It still doesn't contain many information on the many features of the tool & on how to effectively use the tool. Help improve the [documentation](https://github.com/3nock/s3s_doc).*

***Disclaimer 2:** Incase of an unexpected error or erronous results please reach out by openning an [issue](https://github.com/3nock/sub3suite/issues) on the repo or on [Telegram](https://t.me/sub3suite) chat*.

## What is? 

**CIDR -** CIDR (Classless Inter-Domain Routing or supernetting) is a method of assigning Internet Protocol (IP) addresses that improves the efficiency of address distribution
CIDR is based on variable-length subnet masking (VLSM), which enables network engineers to divide an IP address space into a hierarchy of subnets of different sizes, making it possible to create subnetworks with different host counts without wasting large numbers of addresses.
CIDR addresses are made up of two sets of numbers: a prefix, which is the binary representation of the network address -- similar to what would be seen in a normal IP address -- and a suffix, which declares the total number of bits in the entire address. For example, CIDR notation may look like: 192.168.129.23/17 -- with 17 being the number of bits in the address. IPv4 addresses allow a maximum of 32 bits.
[reference](https://www.techtarget.com/searchnetworking/definition/CIDR).

**CIDR Blocks -** CIDR blocks are groups of addresses that share the same prefix and contain the same number of bits. The combination of multiple connecting CIDR blocks into a larger whole, sharing a common network prefix, is what constitutes supernetting.
The size of CIDR blocks can be determined by the length of the prefix. A short prefix allows for more addresses -- and, therefore, forms a bigger block -- while a longer prefix indicates less addresses and a smaller block.
Blocks are initially handled by the Internet Assigned Numbers Authority (IANA). IANA is responsible for distributing large blocks of IP addresses to Regional Internet Registries (RIRs). These blocks are used for large geographical areas, such as North America, Africa and Europe.
[reference](https://www.techtarget.com/searchnetworking/definition/CIDR).

You can obtain CIDR from the [OSINT Engine](../engines/osint.md) and [ASN Enumerator](asn.html) of Sub3 Suite

**CIDR Enumerator -** Is Used to return list useful information about the CIDR. 
sub3suite's CIDR Enumerator queries this data from OSINT sources that provide CIDR Info lookup.

## Input Output 

**Input:** CIDR

**Output:** CIDR Info: owner's address, email contacts, abuser contacts, RIR info and related ASNs

## Features: 

**Multiple Targets search:** Search mulitple targets and the enumerator will provide the results for every targets.


## Scan Configuration values: 

**Timeout -** Time for performing the lookup in milliseconds (terminates connection if timeout). It is advised for the timeout to be greater than 1000

**No Duplicates -** Check to avoid duplicated results of the target

**AutoSave To Project -** Sends the obtained results directly to the project explorer as the scan progresses


## Usage: 

1. Set the scan configuration by clicking the **config** button, setting the values and save.

<img src=images/enum_config.png>

2. Enter Target/Targets;

 a. **If single Target:** enter target (CIDR) on the LineEdit. 
 
 <img src=images/cidr_target.png>
 
 b. **If multiple Targets:** check the **Multile Targes** checkbox and enter the target values (CIDRs) on the ListView marked by **Targets**. 
 
 <img src=images/cidr_targets.png>
 
3. choose the module to use for enumeration.

 <img src=images/cidr_modules.png>

4. Start The scan

5. Several ***Actions*** can be performed on the obtained results.

## Actions: 

Details on the actions for the obtained results.

	<img src=images/enum_actions.png>

 - The Actions on Results are accessible via the **Actions >** button and **Right-Click** on the Results. & are only active when the results are present

1. **Clear:** Clears the results and the progress bar.
2. **Expand & Collapse:** Expands the all areas of the result tree and Collapse all areas of the result tree respectively
3. **Save:** Saves the obtained Results To a File. Saves in Json format
4. **Copy:** Copies the results on the clipboard. Copies in Json format
5. **Send To Project:** Sends the Obtained results to the project explorer.
5. **Send * To ENGINE*/ENUM*:** Sends the Obtained ASN,Emails to the choosen Engine/Enumerator.

**NOTE:**
	If you have filtered the results using the filter. the above actions will only be performed on the remaing results after filter