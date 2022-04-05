# Email Enumerator

***Disclaimer 1:** This is a very simple documentation on the Tool. It still doesn't contain many information on the many features of the tool & on how to effectively use the tool. Help improve the [documentation](https://github.com/3nock/s3s_doc).*

***Disclaimer 2:** Incase of an unexpected error or erronous results please reach out by openning an [issue](https://github.com/3nock/sub3suite/issues) on the repo or on [Telegram](https://t.me/sub3suite) chat*.

## What is? 

**Email -** Email, short for "electronic mail," is one of the most widely used features of the Internet, along with the web. It allows you to send and receive messages to and from anyone with an email address, anywhere in the world.
Email uses multiple protocols within the TCP/IP suite. For example, SMTP is used to send messages, while the POP or IMAP protocols are used to retrieve messages from a mail server
[reference](https://techterms.com/definition/email).

You can obtain Emails of different target types using the [OSINT Engine](../engines/osint.md) of Sub3 Suite

**Email Enumerator -** Is used to return some useful information about the email. 
sub3suite's Email Enumerator queries this data from OSINT sources that provide Email information lookup.

## Input Output 

**Input:** Email
**Output:** Information about the Email

## Features: 

**Multiple Targets search:** Search mulitple targets and the enumerator will provide the results for every targets.


## Scan Configuration values: 

**Timeout -** Time for performing the lookup in milliseconds (terminates connection if timeout). It is advised for the timeout to be greater than 1000
**No Duplicates -** Check to avoid duplicated results of the target
**AutoSave To Project -** Sends the obtained results directly to the project explorer as the scan progresses


## Usage: 

1. Set the scan configuration by clicking the **config** button, setting the values and save.
2. **If single Target:** enter target (email) on the LineEdit. **If multiple Targets:** check the **Multile Targes** checkbox and enter the target values (email) on the ListView marked by **Targets**. 
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
