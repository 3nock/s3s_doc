# SSL ENGINE 

***Disclaimer 1:** This is a very simple documentation on the Tool. It still doesn't contain many information on the many features of the tool & on how to effectively use the tool. Help improve the [documentation](https://github.com/3nock/s3s_doc).*

***Disclaimer 2:** Incase of an unexpected error or erronous results please reach out by openning an [issue](https://github.com/3nock/sub3suite/issues) on the repo or on [Telegram](https://t.me/sub3suite) chat*.

## What is? 

**SSL/TLS -** SSL (Secure Sockets Layer) and its successor, TLS (Transport Layer Security), are protocols for establishing authenticated and encrypted links between networked computers. 
Although the SSL protocol was deprecated with the release of TLS 1.0 in 1999, it is still common to refer to these related technologies as "SSL" or "SSL/TLS". 
[reference](https://www.ssl.com/faqs/faq-what-is-ssl)

**SSL Certificates -** SSL certificates make SSL/TLS encryption possible, and they contain the website's public key and the website's identity, along with related information. 
Devices attempting to communicate with the origin server will reference this file to obtain the public key and verify the server's identity. The private key is kept secret and secure.
[reference](https://www.cloudflare.com/learning/ssl/what-is-an-ssl-certificate)

**SSL Engine -** Is used to enumerate SSL Certificates from targets by actively establishing encrypted connection to the target and pulling the obtained SSL Certificate to
obtain all relevant information stored in the certificate that can be useful to map the target.
SSL Certificates store important information such as:
1. Associated domains.
2. Organization name & contacts.
3. Issued & Expirely date of the certificate. etc

sub3suite's SSL Engine pulls all the data from the SSL Certificate and present it in a very intuitive manner.
The Tool returns results as SSL Certificates full info, SSL Cert Hash(sha1 && sha256) & SSL alternative names.

This Tool uses multiple threads as alocated by the user to perform enumeration.

## Input Output: 

**Input:** Domain/Hostname

**Output:** Alternative/Associated Names, Certicate Hash(sha1/sha256) & The Certificate

## Features: 
1. Supports multiple Targets connections in one scan using multiple threads.
2. Supports enumeration by connecting to host on specified ports eg (HTTP, HTTPS, FTP etc.).
3. **Multiple Targets search:** Search mulitple targets and the enumerator will provide the results for every targets.

## Scan Configuration values: 

<img src=images/ssl_config.png>

**Timeout -** Time for performing the lookup in milliseconds (terminates connection if timeout). It is advised for the timeout to be greater than 1000

**No Duplicates -** Check to avoid duplicated results of the target

**AutoSave To Project -** Sends the obtained results directly to the project explorer as the scan progresses

## Usage & Examples

1. Choose the **output(scan type)** first. **Alternative Names:** pulls alternative/associated names from the SSL certificate **Certificate Hash:** returns the SSL certificate hash(sha1/sha256) 
**SSL Certificate:** returns the SSL Certificate

<img src=images/ssl_output.png>

2. Choose the protocal to connect to. These protocals use TLS for secured connection hence SSL certificates can be pulled from.

<img src=images/ssl_protocal.png>

3. Enter Target/Targets:

	a. for **single target** just enter the targets on the lineEdit.
	
	<img src=images/ssl_target.png>
	
	b. For **multiple targets**; check the **Multiple Targets** checkbox, add your targets to the listView.
	
	<img src=images/ssl_targets.png>

4. **Start** scan. You can **Pause, Resume** and **Stop** the scan.

5. You can also **Re-Scan** failed scans(scans that returned an error) with different configurations.

<img src=images/brute_rescan.png>

6. Several ***Actions*** can be performed on the obtained results.

## Actions: 

Details on the actions for the obtained results.

<img src=images/ssl_actions.png>

 - The Actions on Results are accessible via the **Actions >** button and **Right-Click** on the Results. & are only active when the results are present

1. **Clear:** Clears the results and the progress bar.
2. **Expand & Collapse:** Expands the all areas of the result tree and Collapse all areas of the result tree respectively
3. **Save:** Saves the obtained Results To a File. Saves in Json format
4. **Copy:** Copies the results on the clipboard. Copies in Json format
5. **Send To Project:** Sends the Obtained results to the project explorer.

**NOTE:**
	If you have filtered the results using the filter. the above actions will only be performed on the remaing results after filter
	
## References: 
1. [Use Certificate Transparency for OSINT and passive reconnaissance](https://www.vanimpe.eu/2016/08/29/use-certificate-transparency-osint)
2. [Certificates: The OSINT Gift that Keeps on Giving](https://osintcurio.us/2019/03/12/certificates-the-osint-gift-that-keeps-on-giving)
