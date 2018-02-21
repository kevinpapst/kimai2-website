---
layout: page
title: Kimai v1 - a traditional web-based time tracker
description: Kimai v1 resources - upgrade infos, documentation and links
redirect_from:
  - faq.html
sitemap:
    priority: 0.7
    lastmod: 2018-02-10
    changefreq: weekly
---

<header class="major">
	<h1>Kimai v1</h1>
    <p>
        In the mid of 2018 we will release <b>Kimai v2</b> and stop support for Kimai v1. 
        But as v1 is still widely used, we created this page as backup and your guide in the upgrade process. 
    </p>
</header>

>Feature support for Kimai v1 was stopped with the release of Kimai v2. 
>We will support Kimai v1 until end of 2018 with bugfixes and security related issues.
>Please consider [upgrading as soon as possible](/documentation/upgrade-kimai-v1/)!

## Links

- Find Kimai v1 sources at [GitHub]({{ site.repo_url }})
- Create a new ticket in our [support, bug and issue tracker]({{ site.issues_url }}) 
- You can try our [Kimai v1 demo](demo.html) live

## Download

<ul class="actions">
    <li><a href="{{ site.stable_url }}" class="button special icon fa-download">Stable - 1.1.0</a></li>
    <li><a href="{{ site.repo_url }}/zipball/develop" class="button icon fa-download">Development</a></li>
    <li><a href="https://github.com/kimai/manuals/" class="button icon fa-file-pdf-o">Documentation</a></li>
    <li><a href="apps/" class="button icon fa-archive">Applications</a></li>
</ul>

Server requirements for Kimai v1 are: 

- MySQL 4.3 or higher
- PHP 5.5 or higher
- Required PHP extensions: `mysqli`, `iconv` and `xml`

## Documentation

* [Installation](installation/)
* [Updates](updates/)
* [Upgrade to v2](/documentation/upgrade-kimai-v1/)

### Using Kimai

* [Timesheet](timesheet/)
* [Budget](budget/)
* [Expenses](expenses/)
* [Export](export/)
* [Invoices](invoices/)
* [Rates](rates/)
* [Fees](fees/)
* [Administration](administration/)

### Developer

* [Developer](developer/)
* [Translations](translations/)
* [Invoice templates](invoice-templates/)
* [Authenticator](authenticator/)
* [Extensions](extensions/)
* [Team stuff](team/)

## Other downloads

- Kimai v2 releases can be found at our [GitHub release page]({{ site.kimai_v2_repo }}/releases)
- Kimai v1 releases can be found on the [release page]({{ site.repo_url }}/releases) of the v1 repository
- And historical versions on the [archived download page](https://sourceforge.net/projects/kimai/files/) at Sourceforge
