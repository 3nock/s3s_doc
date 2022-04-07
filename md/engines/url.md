# URL Engine 

***Disclaimer 1:** This is a very simple documentation on the Tool. It still doesn't contain many information on the many features of the tool & on how to effectively use the tool. Help improve the [documentation](https://github.com/3nock/s3s_doc).*

***Disclaimer 2:** Incase of an unexpected error or erronous results please reach out by openning an [issue](https://github.com/3nock/sub3suite/issues) on the repo or on [Telegram](https://t.me/sub3suite) chat*.

## What is? 

URL -** Uniform Resource Locator, colloquially termed a web address, is a reference to a web resource that specifies its location on a computer network and a mechanism for retrieving it. 
A URL is a specific type of Uniform Resource Identifier (URI), although many people use the two terms interchangeably. 
URLs occur most commonly to reference web pages (http/https) but are also used for file transfer (ftp), email (mailto), database access (JDBC), and many other applications.
[reference](https://en.wikipedia.org/wiki/URL).

You can obtain URL from the [OSINT Engine](./engines/osint.html) of Sub3 Suite

## Input Output 

**Input:** URL
**Output:** URL Info: status code, banner(server) and content type

## Features: 

**Multiple Targets search:** Search mulitple targets and the enumerator will provide the results for every targets.


## Scan Configuration values: 

<img src=images/ssl_config.png>

**Threads -** Number of threads to use for quering the targets. If number of threads is greater that the number of targets, then one thread per target will be used.
**Timeout -** Time for performing the lookup in milliseconds (terminates connection if timeout). It is advised for the timeout to be greater than 1000
**No Duplicates -** Check to avoid duplicated results of the target
**AutoSave To Project -** Sends the obtained results directly to the project explorer as the scan progresses

## Usage & Examples

1. Enter Target/Targets:

	a. for **single target** just enter the targets on the lineEdit.
	
	<img src=images/url_target.png>
	
	b. For **multiple targets**; check the **Multiple Targets** checkbox, add your targets to the listView.
	
	<img src=images/url_targets.png>
	
2. **Start** scan. You can **Pause, Resume** and **Stop** the scan.

3. You can also **Re-Scan** failed scans(scans that returned an error) with different configurations.

<img src=images/brute_rescan.png>

4. Several ***Actions*** can be performed on the obtained results.

## Actions: 

Details on the actions for the obtained results.

<img src=images/url_actions.png>

 - The Actions on Results are accessible via the **Actions >** button and **Right-Click** on the Results. & are only active when the results are present

1. **Clear:** Clears the results and the progress bar.
2. **Expand & Collapse:** Expands the all areas of the result tree and Collapse all areas of the result tree respectively
3. **Save:** Saves the obtained Results To a File. Saves in Json format
4. **Copy:** Copies the results on the clipboard. Copies in Json format
5. **Send To Project:** Sends the Obtained results to the project explorer.
5. **Send URL To ENGINE*:** Sends the Obtained URL to the choosen Engine.

**NOTE:**
	If you have filtered the results using the filter. the above actions will only be performed on the remaing results after filter