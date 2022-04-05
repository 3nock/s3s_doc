# RAW ENGINE 

***Disclaimer 1:** This is a very simple documentation on the Tool. It still doesn't contain many information on the many features of the tool & on how to effectively use the tool. Help improve the [documentation](https://github.com/3nock/s3s_doc).*

***Disclaimer 2:** Incase of an unexpected error or erronous results please reach out by openning an [issue](https://github.com/3nock/sub3suite/issues) on the repo or on [Telegram](https://t.me/sub3suite) chat*.

***Disclaimer 3:** Since this Tool is still in its early development stage some queries of some modules may have not been implemented or not well implement such as those withmulitple paremeters or different request types. **Do not worry** since it is work in progress, the modules and query options will be continuously upgraded in the comming versions.You can [contact us](https://github.com/3nock/sub3suite/blob/main/CONTACTS.md) if you need a particular relevant module(OSINT source) be integrated.*

## What is? 
The Raw Engine queries API endpoints of different osint modules to return raw json results.
The tool uses different osint modules and their different endpoints to obtain the desired output.

This Tool does not support multi-threading, uses one thread upon each invocation to perform one lookup after another
even for multiple targets due to rate limits imposed by most osint sources(modules).

## Modules 
The osint modules are mainly categorized in two major groups; Those that require API keys & those that do not require API keys.
They are further categorized into different sub-groups depending on the type that the osint source majorly deals with.

### The Osint Source's Sub-groups 

**--> Iana sub-group:** These are the Osint Sources associated with the Iana.

**--> Certificates sub-group:**  These Osint Sources majorly contains resources associating with SSL Certificates gathered for different sites.

**--> Emails sub-group:** These Osint Sources majorly deals with osint of emails.

**--> API sub-group:** These are Osint Sources that contain a variety of osint API endpoints.

**--> Archives sub-group:** These are Osint Sources containing archives of different internet entities.

## Features 
1. Supports different Input types depending on the endpoint query request
2. Results are returned as Raw json in a TextEdit and also as item-based in a TreeView.
3. Use filters to extract specific entities from the returned json results
2. Supports querying for multiple targets.

## Scan Configuration values: 
**Timeout -** Time for performing the lookup in milliseconds (terminates connection if timeout). It is advised for the timeout to be greater than 1000
**No Duplicates -** Check to avoid duplicated results of the target
**AutoSave To Project -** Sends the obtained results directly to the project explorer as the scan progresses

## Example & Usage:

1. First Choose the `OSINT module` you want use.

	<img src=images/raw_module.png>
	
	***NOTE:**
	
	For modules in the **API Keys Required** category you must have an API Key to query that module. You can obtain API Keys by opening API Keys Module -> scroll to your module of choice and
	click **Get...** and it will direct you to the page where you can obtain the API key, Enter the Key and Save.
	
	<img src=images/raw_key.png>
	
	<img src=images/apikeys.png>
	
2. Then choose the `query option` (API Endpoint).

	<img src=images/raw_endpoint.png>
	
3. Enter Target/Targets:

	a. for **single target** just enter the targets on the lineEdit.
	
	<img src=images/raw_target.png>
	
	b. For **multiple targets**; check the **Multiple Targets** checkbox, goto Targets Tab and add your targets to the listView.
	
	<img src=images/raw_targets.png>
	
4. Start the Scan. click `Start` to Start the scan and wait for results.

5. Results are displayed in two tabs. 

	a. `Results Tab` (which shows raw json results)
	
	<img src=images/raw_results.png>
	
	b. `Tree Tab` (which shows json results in a tree view)
	
	<img src=images/raw_tree.png>
	
6. You can double-click on a particular object(item) on the tree to view it in json format in `Json Tab`

	<img src=images/raw_item.png>
	
	<img src=images/raw_json.png>
	

5. Several `Actions` can be performed on the obtained results.

## Actions: 

Details on the actions for the obtained results.

 - The Actions on Results are accessible via the **Actions >** button and **Right-Click** on the Results. & are only active when the results are present

1. **Clear:** Clears the results and the progress bar.
2. **Expand & Collapse:** Expands the all areas of the result tree and Collapse all areas of the result tree respectively
3. **Save:** Saves the obtained Results To a File. Saves in Json format
4. **Copy:** Copies the results on the clipboard. Copies in Json format
5. **Send To Project:** Sends the Obtained results to the project explorer.
6. **Send Item:** Sends The choosen Item Type to appropriate ENGINE/ENUMERATOR.

**NOTE:**
	If you have filtered the results using the filter. the above actions will only be performed on the remaing results after filter