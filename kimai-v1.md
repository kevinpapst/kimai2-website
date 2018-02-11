---
layout: page
title: Kimai v1
description: Kimai v1 resources - upgrade infos, documentation and links
permalink: /v1/
sitemap:
    priority: 0.7
    lastmod: 2018-02-10
    changefreq: weekly
---

<header class="major">
	<h1>Kimai v1</h1>
    <p>
        In the mid of 2018 we released <b>Kimai v2 reloaded</b> and stopped support for Kimai v1. 
        But we know its still widely used and we want to make the upgrade process as smooth as possible for our users. 
    </p>
</header>

>Feature support for Kimai v1 was stopped with the release of Kimai v2. 
>We will support Kimai v1 until end of 2018 with bugfixes and security related issues.
>Please consider upgrading as soon as possible!

## Links

- Find Kimai v1 sources at [GitHub]({{ site.repo_url }})
- Create a new ticket in our [support, bug and issue tracker]({{ site.issues_url }}) 
- [Kimai v1 documentation]({{ site.docu_url }})

## Download

<ul class="actions">
    <li><a href="{{ site.stable_url }}" class="button special icon fa-download">Stable - 1.1.0</a></li>
    <li><a href="{{ site.repo_url }}/zipball/develop" class="button icon fa-download">Development</a></li>
    <li><a href="https://github.com/kimai/manuals/raw/master/documentation.pdf" class="button icon fa-file-pdf-o">Documentation</a></li>
    <li><a href="/apps/" class="button icon fa-archive">Applications</a></li>
</ul>

Server requirements for Kimai v1 are: 

- MySQL 4.3 or higher
- PHP 5.4 or higher
- Required PHP extensions: `mysqli`, `iconv` and `xml`

### Installation

1. Start your browser and go to your Kimai directory
2. Kimai has a step-by-step installation program, just follow the instructions of the installer
3. **IMPORTANT:** Remove the `installer` and `updater` directory when you’ve successfully installed Kimai

### Update Kimai v1

When you update an existing installation, just replace the entire Kimai folder on your server. Additionally you need to make the `temporary` folder writable for PHP. 
Open Kimai in your browser and follow the upgrade guide. Afterwards remove the `installer` and `updater` directories.

Read more about it in our official [update documentation]({{ site.docu_url }}installation/updates.html).

## Upgrade to Kimai v2

*You have to install Kimai v2 first, please read the documentation at [GitHub]({{ site.kimai_v2_repo }}).
We recommend installing it on the same server, as long as you can meet the PHP7 requirement.*

Before importing your data from a Kimai v1 installation, please read the following carefully:

- Data from an existing v1 installation can be imported, it will only be read and never be changed
- Data can only be imported from a Kimai installation with at least `v1.0.1` and database revision `1388` (check your `configuration` table)
- Kimai v1 has support for activities without project assignment, which Kimai v2 doesn't support. Unattached activities will be created for every project that has a linked activity in any of the imported timesheet records
- Rates and fixed-rates are handled in a completely different way and for now only the timesheet record total amounts are imported
- Customers cannot login and no user accounts will be created for them
- The customers country has to be manually assigned afterwards, as there is no field in Kimai v1 for that
- You have to supply a default password that all imported user, as their password will be reset
- Data that was deleted in Kimai v1 (user, customer, projects, activities) will be imported and set to `invisible` (if you don't want that, you have to delete all entries that have the value `1` in the `trash` column before importing)

A possible full command for import:
{% highlight bash %}
bin/console kimai:import-v1 "mysql://user:password@127.0.0.1:3306/database?charset=utf8" "db_prefix" "password" "country"
{% endhighlight %}

It is recommended to test the import in a fresh database. You can test your import as often as you like and fix possible problems in your installation.

A sample command could look like that:
{% highlight bash %}
bin/console doctrine:schema:drop --force && bin/console doctrine:schema:create && bin/console kimai:import-v1 "mysql://kimai:test@127.0.0.1:3306/kimai?charset=latin1" "kimai_" "test123" "de"
{% endhighlight %}

That will drop the configured Kimai v2 database schema and re-create it, before importing the data from the `mysql` database at `127.0.0.1` on port `3306` authenticating the user `kimai` with the password `test` for import.
The connection will use the charset `latin1` and the default table prefix `kimai_` for reading data. Imported users can login with the password `test123` and all customer will have the country `de` assigned.

