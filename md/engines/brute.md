# BRUTE ENGINE 

***Disclaimer 1:** This is a very simple documentation on the Tool. It still doesn't contain many information on the many features of the tool & on how to effectively use the tool. Help improve the [documentation](https://github.com/3nock/s3s_doc).*

***Disclaimer 2:** Incase of an unexpected error or erronous results please reach out by openning an [issue](https://github.com/3nock/sub3suite/issues) on the repo or on [Telegram](https://t.me/sub3suite) chat*.

## What is? 
The BRUTE Engine performs subdomain & TLD enumeration by bruteforce.
Performs DNS lookup on subdomain & TLD created by appending the words from wordlist to the
target.
The tool accomplishes this by resolving the targets using the public nameservers or internal nameservers as provided
by the user.
The domains are resolved to either A(ipv4) or AAAA(ipv6) dns records depending on the scan configuration by user.
The resolved subdomains or TLDs does not necessarily mean the targets are active but an indicator that they can be resolved by
the particular nameservers.

This Tool uses multiple threads as alocated by the user to perform DNS lookup on targets also support use of multiple nameservers as provided
by the user or default list by s3s.

You can obtain Passive Domains/Hostnames from the [OSINT Engine](../engines/osint.md) of Sub3 Suite

## Features 
1. Supports use of multiple nameservers.
2. Supports A(ipv4) and AAAA(ipv6) dns records lookups.
3. Supports subdomain(e.g. *.example.com) and Top-level-domain(TLD e.g. example.*) bruteforcing.
4. Supports multiple Targets lookup in one scan (one target after another).
5. Has a simple wordlist generator(still an early feature, will be advanced later).

## Input Output: 
**Input:** Domain/Hostname

**Output:** Resolved Domain, IPv4 & IPv6

## Scan Configuration values: 

<img src=images/brute_config.png>

**Threads -** Number of threads to use for quering the targets. If number of threads is greater that the number of targets, then one thread per target will be used.

**Timeout -** Time for performing the lookup in milliseconds (terminates connection if timeout). It is advised for the timeout to be greater than 1000

**Record Type -** Record Type to lookup, A(IpV4), AAAA(IpV6), ANY(IpV4 and/or IpV6).

**Wildcard -** Check if you want to detect and mitigate wildcards e.g *.example.com

**No Duplicates -** Check to avoid duplicated results of the target

**AutoSave To Project -** Sends the obtained results directly to the project explorer as the scan progresses

<img src=images/brute_nameservers.png>

**Nameservers -** - Nameservers to use for DNS lookup. You can choose; 

***single nameserver:*** by checking the single nameserver radio-button and choose the nameserver in the combo-box

***random nameserver:*** by checking the random nameserver radio-button and Sub3 Suite will use its default set of nameservers, assigning them randomly

***custom nameserver:*** by checking the random nameserver radio-button and enter the ip addresses of the nameservers you want to use

## Wordlist 
Wordlist for bruteforcing subdomain names. Sub3 Suite has a wordlist feature where you can choose or generate wordlist for bruteforcing subdomains/TLD

<h3> In Choose </h3>

<img src=images/brute_choose_wl.png>
You have the option to choose ***Default wordlist*** that comes with with Sub3 Suite or ***Custom wordlist*** which you have saved

<img src=images/brute_custom_wl.png>
An option to create and save a new custom wordlist that you can use later on

<h3> In Generate </h3>

You can generate wordlist from within Sub3 Suite;

<img src=images/brute_generate_wl.png>

To Generate wordlist, **check the box** of the type of wordlist you want to generate enter the required information and generate.

***A-Z: *** Generates worldist by combining the alphabet characters. Enter the number of combinations you want and generate ie. **1:** no combination e.g A, B, C etc **2:** combination of two alphabets e.g. AA, AB, AC etc. It is recomended to to put a combination count of more than 5 as it will weigh down on the machine's processing power and memory

***Numbers: *** Generates numbers as a wordlist. Any range of numbers can be generated.

***Dates: *** Generates dates as a wordlist.

***Substitution(hymoglyphs): *** Generate wordlist by substituting characters from the input wordlist creating hymoglyphs wordlist. e.g. if you **input:** *google.com* it will **output:** *go0gle.com,go0gle.com,g00gle.com,qoogle.com,q00gle.com* etc. It is recommended
not to input a large wordlist for substitution wordlist generation as it takes much computing power and memory.

## Usage & Examples

1. Choose the **output(scan type)** first. **Subdomain:** does subdomain enumeration and **TLD:** does Top level domain enumeration

<img src=images/brute_output.png>

2. **Enter/Choose/Generate** wordlist to be used for bruteforcing.

<img src=images/brute_wordlist.png>

3. Enter Target/Targets:

	a. for **single target** just enter the targets on the lineEdit.
	
	<img src=images/brute_target.png>
	
	b. For **multiple targets**; check the **Multiple Targets** checkbox, add your targets to the listView.
	
	<img src=images/brute_targets.png>
	
4. **Start** scan. You can **Pause, Resume** and **Stop** the scan.

5. You can also **Re-Scan** failed scans(scans that returned an error) with different configurations.

<img src=images/brute_rescan.png>

5. Several ***Actions*** can be performed on the obtained results.

## Actions: 

Details on the actions for the obtained results.

<img src=images/brute_actions.png>

 - The Actions on Results are accessible via the **Actions >** button and **Right-Click** on the Results. & are only active when the results are present

1. **Clear:** Clears the results and the progress bar.
2. **Expand & Collapse:** Expands the all areas of the result tree and Collapse all areas of the result tree respectively
3. **Save:** Saves the obtained Results To a File. Saves in Json format
4. **Copy:** Copies the results on the clipboard. Copies in Json format
5. **Send To Project:** Sends the Obtained results to the project explorer.
5. **Send * To *:** Sends the Result Type to the choosen Engine/Enumerator.

**NOTE:**
	If you have filtered the results using the filter. the above actions will only be performed on the remaing results after filter