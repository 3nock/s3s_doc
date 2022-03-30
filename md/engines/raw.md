# RAW ENGINE

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
**--> Scrape sub-group:** These are Osint modules that obtain data by scrapping the indicated search engine.
**--> Site sub-group:** These are Osint modules that obtain data from different website containing osint info.

## Features 

1. Supports different Input types depending on the endpoint query request
2. Results are returned as Raw json in a TextEdit and also as item-based in a TreeView.
3. Use filters to extract specific entities from the returned json results
2. Supports querying for multiple targets.

## Usage & Examples

<img src="images/raw_1.png">

<img src="images/raw_2.png">

Help improve the [documentation](https://github.com/3nock/s3s_doc)

## References

1. (https://blog.appsecco.com/a-penetration-testers-guide-to-sub-domain-enumeration-7d842d5570f6)

## NOTE:

*This is a very simple documentation on the Tool. It still doesn't contain many information on the many features of the tool & on how to effectively use the tool.*

*Help improve the [documentation](https://github.com/3nock/sub3suite_doc).*