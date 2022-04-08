# NS Enumerator

***Disclaimer 1:** This is a very simple documentation on the Tool. It still doesn't contain many information on the many features of the tool & on how to effectively use the tool. Help improve the [documentation](https://github.com/3nock/s3s_doc).*

***Disclaimer 2:** Incase of an unexpected error or erronous results please reach out by openning an [issue](https://github.com/3nock/sub3suite/issues) on the repo or on [Telegram](https://t.me/sub3suite) chat*.

## What is? 

**NameServer(NS) -** A name server translates domain names into IP addresses. This makes it possible for a user to access a website by typing in the domain name instead of the website's actual IP address. For example, when you type in "www.microsoft.com," the request gets sent to Microsoft's name server which returns the IP address of the Microsoft website. 
Each domain name must have at least two name servers listed when the domain is registered. These name servers are commonly named ns1.servername.com and ns2.servername.com, where "servername" is the name of the server. The first server listed is the primary server, while the second is used as a backup server if the first server is not responding.
[reference](https://techterms.com/definition/nameserver).

You can obtain NameServer of a domain using the [DNS Engine](../engines/dns.md) of Sub3 Suite

**NS Enumerator -** Is Used to return list  of domains that share the same primary name server. 
sub3suite's NS Enumerator queries this data from OSINT sources that provide reverse Nameserver lookup.

## Input Output 

**Input:** Nameserver

**Output:** Domains

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

 a. **If single Target:** enter target (nameserver) on the LineEdit. 
 
 <img src=images/ns_target.png>
 
 b. **If multiple Targets:** check the **Multile Targes** checkbox and enter the target values (nameserver) on the ListView marked by **Targets**. 
 
 <img src=images/ns_targets.png>
 
3. choose the module to use for enumeration.

 <img src=images/ns_modules.png>

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
5. **Send Hostname To ENGINE*:** Sends the Obtained hostnames/domains to the choosen Engine.

**NOTE:**
	If you have filtered the results using the filter. the above actions will only be performed on the remaing results after filter
