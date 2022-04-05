# OSINT ENGINE 

*** Disclaimer 1:** This is a very simple documentation on the Tool. It still doesn't contain many information on the many features of the tool & on how to effectively use the tool.
Help improve the <a href=https://github.com/3nock/s3s_doc> documentation </a>.</i>

*** Disclaimer 2:** Incase of an unexpected error or erronous results please reach out by openning an <a href=https://github.com/3nock/sub3suite/issues>issue</a> on the repo or on Telegram chat</i>.

## What is? 
The Osint engine is used for obtaining different types of osint data from different input types.
The tool uses different osint modules to obtain the desired data.

Each Module gets its own thread for querying the same targets. for multiple targets the thread queries on target after
another due to query request's rate limits impossed by most modules.

## Modules 
The osint engine uses different osint source to obtain its results.
The osint modules are mainly categorized in two major groups; Those that require API keys & those that do not require API keys.
They are further categorized into different sub-groups depending on the type that the osint source majorly deals with.

### The Osint Source's Sub-groups 
**--> Certificates sub-group:**  These Osint Sources majorly contains resources associating with SSL Certificates gathered for different sites.
**--> Emails sub-group:** These Osint Sources majorly deals with osint of emails.
**--> API sub-group:** These are Osint Sources that contain a variety of osint API endpoints.
**--> Archives sub-group:** These are Osint Sources containing archives of different internet entities.
**--> Scrape sub-group:** These are Osint modules that obtain data by scrapping the indicated search engine.
**--> Site sub-group:** These are Osint modules that obtain data from different website containing osint info.

## Features 
1. Supports different Input types to different Output types.
2. Supports querying for multiple targets.

### Input Types 
1. Hostname.
2. Ip Address.
3. Email.
4. Url.
5. ASN.
6. SSL Certificate Hash.
7. CIDR.

### Output Types 
1. Subdomains.
2. Subdomain & Ip.
3. Ip Address.
4. Email.
5. Url.
6. ASN.
7. SSL Certificate Hash.
8. CIDR.

The User can choose the input type, out type and module to pull data from.

## Scan Configuration values: 
You can set configurations for your scan to run on. click ** config **, set the values and save the values
** Timeout - ** Time for performing the lookup in milliseconds (terminates connection if timeout). It is advised for the timeout to be greater than 1000
** No Duplicates - ** Check to avoid duplicated results of the target
** AutoSave To Project - ** Sends the obtained results directly to the project explorer as the scan progresses


## Example & Usage 
To use the OSINT Engine for enumeration take the following steps:

1. Choose The Input and Output type for your scan i.e. if you want to obtain subdomains from an IpAddress then choose an input as IpAddress and output as Subdomains
   e.g 
   
   <img src=images/osint_input.png>
   
2.Enter Target/Targets:

	a. for single target just enter the targets on the lineEdit.
	
	<img src=images/osint_target.png>
	
	b. For multiple targets; check the ** Multiple Targets ** checkbox and add your targets to the listView.
	
	<img src=images/osint_targets.png>
	
3. Choose OSINT modules to use. Check the check-boxes of the modules you want to pull data from. You can check from one to as many as you want.

	<img src=images/osint_modules.png>
	
	*** NOTE:**
	
	For modules in the ** API Keys Required** category you must have an API Key to query that module. You can obtain API Keys by opening API Keys Module -> scroll to your module of choice and
	click ** Get... ** and it will direct you to the page where you can obtain the API key, Enter the Key and Save.
	
	<img src=images/osint_key.png>
	
	<img src=images/apikeys.png>
	
4. Start the Scan. click Start to Start the scan and wait for results.

5. After the scan is finished and you've obtained the results, several actions can be performed on the obtained results.

## Actions: 

Details on the actions for the obtained results.

 - The Actions on Results are accessible via the **Actions >** button and **Right-Click** on the Results. & are only active when the results are present

1. ** Clear: ** Clears the results and the progress bar.
2. ** Expand & Collapse: ** Expands the all areas of the result tree and Collapse all areas of the result tree respectively
3. ** Save: ** Saves the obtained Results To a File. Saves in Json format
4. ** Copy: ** Copies the results on the clipboard. Copies in Json format
5. ** Send To Project: ** Sends the Obtained results to the project explorer.
5. ** Send * To *: ** Sends the Result Type to the choosen Engine/Enumerator.

** NOTE: **
	If you have filtered the results using the filter. the above actions will only be performed on the remaing results after filter