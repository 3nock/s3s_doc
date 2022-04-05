# MX Enumerator 

***Disclaimer 1:** This is a very simple documentation on the Tool. It still doesn't contain many information on the many features of the tool & on how to effectively use the tool. Help improve the [documentation](https://github.com/3nock/s3s_doc).*

***Disclaimer 2:** Incase of an unexpected error or erronous results please reach out by openning an [issue](https://github.com/3nock/sub3suite/issues) on the repo or on [Telegram](https://t.me/sub3suite) chat*.

## What is? 

**MailServer(MX) -** A mail server (or email server) is a computer system that sends and receives email. In many cases, web servers and mail servers are combined in a single machine. However, large ISPs and public email services (such as Gmail and Hotmail) may use dedicated hardware for sending and receiving email.
In order for a computer system to function as a mail server, it must include mail server software. This software allows the system administrator to create and manage email accounts for any domains hosted on the server. 
For example, if the server hosts the domain name "techterms.com," it can provide email accounts ending in "@techterms.com.".
[reference](https://techterms.com/definition/mail_server).

You can obtain MailServer of a domain using the [DNS Engine](../engines/dns.md) of Sub3 Suite

**MX Enumerator -** Is Used to return list  of domains that share the same primary mail server. 
sub3suite's MX Enumerator queries this data from OSINT sources that provide reverse MailServer lookup.

## Input Output 

**Input:** MailServer
**Output:** Domains

## Features: 

**Multiple Targets search:** Search mulitple targets and the enumerator will provide the results for every targets.


## Scan Configuration values: 

**Timeout -** Time for performing the lookup in milliseconds (terminates connection if timeout). It is advised for the timeout to be greater than 1000
**No Duplicates -** Check to avoid duplicated results of the target
**AutoSave To Project -** Sends the obtained results directly to the project explorer as the scan progresses


## Usage: 

1. Set the scan configuration by clicking the **config** button, setting the values and save.
2. **If single Target:** enter target (mail_server) on the LineEdit. **If multiple Targets:** check the **Multile Targes** checkbox and enter the target values (mail_server) on the ListView marked by **Targets**. 
3. Start The scan

## Actions: 

Details on the actions for the obtained results.

 - The Actions on Results are accessible via the **Actions >** button and **Right-Click** on the Results. & are only active when the results are present

1. **Clear:** Clears the results and the progress bar.
2. **Expand & Collapse:** Expands the all areas of the result tree and Collapse all areas of the result tree respectively
3. **Save:** Saves the obtained Results To a File. Saves in Json format
4. **Copy:** Copies the results on the clipboard. Copies in Json format
5. **Send To Project:** Sends the Obtained results to the project explorer.
5. **Send Hostname To ENGINE*:** Sends the Obtained hostnames/domains to the choosen Engine.

**NOTE:**
	If you have filtered the results using the filter. the above actions will only be performed on the remaing results after filter
