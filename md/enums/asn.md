# ASN Enumerator 

***Disclaimer 1:** This is a very simple documentation on the Tool. It still doesn't contain many information on the many features of the tool & on how to effectively use the tool. Help improve the [documentation](https://github.com/3nock/s3s_doc).*

***Disclaimer 2:** Incase of an unexpected error or erronous results please reach out by openning an [issue](https://github.com/3nock/sub3suite/issues) on the repo or on [Telegram](https://t.me/sub3suite) chat*.

## What is? 

**ASN -** An autonomous system number(ASN) is a unique identifier that is globally available and allows its autonomous system to exchange routing information with other systems.
An autonomous system (AS) is a group of IP prefixes with a clearly defined external routing policy. In order for multiple autonomous systems to interact, each needs to have a unique identifier. 
Autonomous system numbers can be public or private. Public ASNs are required for systems to exchange information over the Internet. 
A private ASN can be used instead if a system is communicating solely with a single provider via Border Gateway Protocol (BGP).
[reference](https://blog.stackpath.com/autonomous-system-number).

You can obtain ASN from the [OSINT Engine](../engines/osint.md) and [CIDR Enumerator](cidr.md) of Sub3 Suite

**ASN Enumerator -** Is Used to return list useful information about the ASN. 
sub3suite's ASN Enumerator queries this data from OSINT sources that provide ASN Info lookup.

## Input Output 

**Input:** ASN

**Output:** ASN Info: owner's address, email contacts, abuser contacts, RIR info and related ASNs & CIDR

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

 a. **If single Target:** enter target (ASN) on the LineEdit. 
 
 <img src=images/asn_target.png>
 
 b. **If multiple Targets:** check the **Multile Targes** checkbox and enter the target values (ASNs) on the ListView marked by **Targets**. 
 
 <img src=images/asn_targets.png>
 
3. choose the module to use for enumeration.

 <img src=images/asn_modules.png>

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
5. **Send * To ENGINE*/ENUM*:** Sends the Obtained ASN,CIDR,Emails to the choosen Engine/Enumerator.

**NOTE:**
	If you have filtered the results using the filter. the above actions will only be performed on the remaing results after filter
	
## References: 
1. [What is an Autonomous System Number (ASN)?](https://blog.stackpath.com/autonomous-system-number)
2. [ASN Lookup Tools, Strategies and Techniques](https://securitytrails.com/blog/asn-lookup)
3. [Passive Subdomain Enumeration](https://niiconsulting.com/checkmate/2020/09/passive-subdomain-enumeration-part-1)