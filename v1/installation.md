---
layout: documentation
title: Documentation for Kimai
description: Documentation for Kimai Time-Tracking
---
# Installation

1. Start your browser and go to your Kimai directory
2. Kimai has a step-by-step installation program, just follow the instructions of the installer
3. **IMPORTANT:** Remove the `installer` and `updater` directory when you’ve successfully installed Kimai

And here comes the long version:

## Requirements

The following requirements must be met on the server installation:

* PHP version 5.4 or higher (not tested with PHP 7.2 yet)
- PHP extensions: `mysqli`, `iconv` and `xml`
* MySQL 4.3 or higher (Kimai supports table prefixes)
* FTP or shell access to set the correct filesystem permissions

## Installation on Ubuntu

* Install apache (or any other webserver)
* Install mysqli
* Install php
* Install additional required module php-xml with ``sudo apt-get install php-xml``

Extract the Kimai release zip/tarball into a server directory accessible from the outside and navigate to this location using your browser. A step-by-step installation program is included with every new release of Kimai. Follow the instructions of the installer and correct missing or incorrect permissions using your FTP or shell account. 
If the step-by-step installer does not work, [please report this error]({{ site.issues_url }}).

Remove the “install” directory after the installation!

After you removed the “install” directory you may login into Kimai using the following credentials:

* user: admin
* password: changeme

Change the administrator password using the settings dialog. Keeping “changeme” as your password is a major security implication!

