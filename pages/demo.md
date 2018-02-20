---
layout: page
title: Kimai demo installation - test time-tracking
description: You can test and evaluate our time-tracker Kimai online, directly from our page.
permalink: /demo/
redirect_from:
  - /en/demo.html
  - /demo.html
---

<header class="major">
	<h1>Demo</h1>
    <p>
    Try out the [Kimai time-tracking demo]({{ site.kimai_v2_demo }}) and we promise: your next step will be the <a href="{{ site.download_url }}">download</a> 
    </p>
</header>

This page leads you to a [demo installation]({{ site.kimai_v2_demo }}) of Kimai, where you can get a first
impression on how this software feels and which functionality it provides.
If you encounter any problem, we would kindly ask you to send us a [message in our issue tracker]({{ site.kimai_v2_repo }}/issues).
Please notice, that the Demo will be reinstalled on a regular schedule and all entered data will be removed.

## Demo users

The following user are available for your test purpose. Please create your own test user (see below) if these don't work:

| Username | Password | Role |
|---|:---:|---|
| john_user | kitten | User |
| chris_user | kitten | User (deactivated) |
| tony_teamlead | kitten | Teamlead |
| anna_admin | kitten | Administrator |
| susan_super | kitten | Super-Administrator |
| admin | password | Super-Administrator |

## Demo state & new test user

The demo url is: [{{ site.kimai_v2_demo }}]({{ site.kimai_v2_demo }})

<script src="https://demo-v2.kimai.org/status.js"></script>

## Note

- The demo is always created from the latest master branch
- It's possible that you find bugs which will not be available in a release version
- The Kimai demo will be reinstalled twice a day, make sure that you don't run into a reinstall while performing your tests
- The demo imports the default test fixtures that is shipped with Kimai v2, so you can start with a decent amount of data 
