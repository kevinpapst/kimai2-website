---
layout: documentation
title: Upgrade to Kimai v2
description: Upgrading your Kimai installation to Kimai 2 coming from v1
---

## Upgrade to Kimai 2 (from v1)

*You have to install Kimai v2 first, please read the documentation at [GitHub]({{ site.kimai_v2_repo }}).
You can install it on the same server, but remember that you have to meet the PHP7 requirement.*

Before importing your data from a Kimai v1 installation, please read the following carefully:

- Data from the existing v1 installation is only read and will never be changed
- Data can only be imported from a Kimai installation with at least `v1.0.1` and database revision `1388` (check your `configuration` table)
- User-specific rates are not yet supported in Kimai 2
  - fixed-rates and hourly-rates for projects and activities are imported
  - fixed-rates and hourly-rates and total rate for timesheet entries are imported
- Customers in Kimai 2 are only used for recording
  - they cannot login and no user accounts will be created for them
  - country has to be manually assigned afterwards to customers, as there is no field in Kimai v1 for that
- You have to supply the default password that is used for every imported user, as their password will be resetted
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

