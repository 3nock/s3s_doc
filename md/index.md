# Getting started with Sub3 Suite

## Launching 

Download Sub3 Suite for your required platform (Windows, MacOS, or Linux) from [releases](https://github.com/3nock/sub3suite/releases).
Launch Sub3 Suite by clicking the sub3suite application.

## Startup wizard

When Sub3 Suite launches, the startup wizard is displayed. This lets you choose what s3s project to open.

### Selecting a project

You can choose from the following options to create or open a project:

`Temporary project` - This option is useful for quick tasks where your work doesn't need to be saved. All data is held in memory, and is lost when s3s exits.

`New project on disk` - This creates a new project that will store its data in a Sub3 project file. This file will hold all of the data and configuration for the project, and data is saved incrementally as you work. You can also specify a name for the project.

`Open existing project` - This reopens an existing project from a Sub3 project file. A list of recently opened projects is shown for quick selection. When this option is selected, the Spider and Scanner tools will be automatically paused when the project reopens, to avoid sending any unintentional requests to existing configured targets. You can deselect this option if preferred.

**Note:**

 You can rename a project later via project config.

## Tools Suite

Use the links below for further help on Sub3 Suite Engines:

1. [Osint](engines/osint.html) Engine.
2. [Raw]((engines/raw.md) Engine.
3. [Brute](engines/brute.md) Engine.
4. [Active](engines/active.md) Engine.
5. [DNS](engines/dns.md) Engine.
6. [SSL](engines/ssl.md) Engine.

Use the links below for further help on Sub3 Suite Enumerators:

1. [IP](enums/ip.md) Enumerator.
2. [ASN](enums/asn.md) Enumerator.
3. [CIDR](enums/cidr.md) Enumerator.
4. [NS](enums/ns.md) Enumerator.
5. [MX](enums/mx.md) Enumerator.
6. [SSL](enums/ssl.md) Enumerator.
7. [Email](enums/email.md) Enumerator.
8. [URL](enums/url.md) Enumerator.