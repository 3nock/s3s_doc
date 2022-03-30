# SSL ENGINE

# What is? 

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

## Features 

1. Supports multiple Targets connections in one scan using multiple threads.
2. Supports enumeration by connecting to host on specified ports eg (HTTP, HTTPS, FTP etc.).

## Usage & Examples

<img src="images/ssl_1.png">

<img src="images/ssl_2.png">

Help improve the [documentation](https://github.com/3nock/s3s_doc)

## References


## NOTE:

*This is a very simple documentation on the Tool. It still doesn't contain many information on the many features of the tool & on how to effectively use the tool.*

*Help improve the [documentation](https://github.com/3nock/sub3suite_doc).*