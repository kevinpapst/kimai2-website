---
title: Kimai 1 is tracking your times since 2007
description: Kimai v1 resources - upgrade infos, documentation and links
subtitle: "Oldie but goldie!"
header: Kimai
redirect_from:
  - faq.html
sitemap:
    priority: 0.7
    lastmod: 2018-02-10
    changefreq: weekly
---

<a href="{{ site.stable_url }}" class="btn btn-primary"><i class="fas fa-download"></i> Download</a>
<a href="{{ site.repo_url }}" class="btn btn-primary"><i class="fab fa-github"></i> GitHub</a>
<a href="demo.html" class="btn btn-primary"><i class="fas fa-plane-departure"></i> Demo</a>
<a href="https://github.com/kimai/manuals/" class="btn btn-primary"><i class="fas fa-book"></i> Documentation</a>
<a href="apps/" class="btn btn-primary"><i class="fas fa-cubes"></i> Applications</a>

### Server requirements

Kimai 1 requires at least: 

- MySQL 4.3 or higher
- PHP 5.5 or higher
- Required PHP extensions: `mysqli`, `iconv` and `xml`

{% for group in site.data.menu-v1 %}
<h3>{{ group.title }}</h3>
<ul>
    {% for p in group.pages %}
    {% assign doc = site.v1 | where: "slug", p | first %}
    <li><a href="{{ doc.url }}">{{ doc.title }}</a></li>
    {% endfor %}
</ul>
{% endfor %}

## More downloads

- Kimai v2 releases can be found at our [GitHub release page]({{ site.kimai_v2_repo }}/releases)
- Kimai v1 releases can be found on the [release page]({{ site.repo_url }}/releases) of the v1 repository
- And historical versions on the [archived download page](https://sourceforge.net/projects/kimai/files/) at Sourceforge
