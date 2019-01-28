---
layout: post
title: "Kimai v2 - Release 0.7"
date: "2019-01-28 02:00:00 +0200"
author: kevinpapst
---

Sorry for the long period of silence! The release of this version took a longer then expected, 
as I moved to a new city and had troubles getting my provider to setup the internet connection. 

[Full Changelog](https://github.com/kevinpapst/kimai2/compare/0.6.1...0.7)

**The release main topic was "permissions". Most notable changes:**

- Configurable permission system
- Limit the amount of active time records per user
- Export team timesheets
- A lot of form and UI improvements (e.g. entry order and icons)
- Load filtered data via toolbar without page reload

**Upgrade from 0.6:**

Don't forget to execute the database migrations! Read more about upgrading Kimai in [UPGRADING](https://github.com/kevinpapst/kimai2/blob/master/UPGRADING.md).

**Implemented enhancements:**

- Editing from calendar view will return to my times table instead of calendar [\#515](https://github.com/kevinpapst/kimai2/issues/515)
- Timesheet Export for Admins [\#503](https://github.com/kevinpapst/kimai2/issues/503)
- Customer List Not Alphabetic [\#499](https://github.com/kevinpapst/kimai2/issues/499)
- sorting of ${entry.X} values [\#487](https://github.com/kevinpapst/kimai2/issues/487)
- ${entry.description} needed in Word-Docx [\#485](https://github.com/kevinpapst/kimai2/issues/485)
- Automatic sort for activities, customers, etc. [\#477](https://github.com/kevinpapst/kimai2/issues/477)
- User title in the timesheet invoice [\#461](https://github.com/kevinpapst/kimai2/issues/461)
- global variables for reports/invoices [\#438](https://github.com/kevinpapst/kimai2/issues/438)
- Configuration option: Only one active record for each user [\#427](https://github.com/kevinpapst/kimai2/issues/427)
- User creating activity and projects [\#393](https://github.com/kevinpapst/kimai2/issues/393)
- Configuration option to disable fixed rate and hourly rate from "edit timesheet" [\#330](https://github.com/kevinpapst/kimai2/issues/330)
- Set other users hourly rate [\#303](https://github.com/kevinpapst/kimai2/issues/303)
- Feature request - Make "Rate" hideable [\#217](https://github.com/kevinpapst/kimai2/issues/217)
- fixed null project for advanced invoice calculator [\#462](https://github.com/kevinpapst/kimai2/pull/462) ([kevinpapst](https://github.com/kevinpapst))

**Fixed bugs:**

- This value should be greater than or equal to zero [\#511](https://github.com/kevinpapst/kimai2/issues/511)
- Timesheet Export for Admins [\#503](https://github.com/kevinpapst/kimai2/issues/503)
- admin activity: visibility "none" \(no filter\) causes sql-error [\#491](https://github.com/kevinpapst/kimai2/issues/491)
- login-screen optimizations [\#483](https://github.com/kevinpapst/kimai2/issues/483)
- Configuration of roles to add/edit customers, projects, activities... [\#479](https://github.com/kevinpapst/kimai2/issues/479)
- Line breaks for address and payment information fields [\#464](https://github.com/kevinpapst/kimai2/issues/464)
- Possible to use a decimal in hourly rate field? [\#458](https://github.com/kevinpapst/kimai2/issues/458)
- Invoice Number Generator possibly not compatible  [\#454](https://github.com/kevinpapst/kimai2/issues/454)
- users can change their role to system-admin [\#440](https://github.com/kevinpapst/kimai2/issues/440)
- fix wrong include filename in user registration [\#520](https://github.com/kevinpapst/kimai2/pull/520) ([kevinpapst](https://github.com/kevinpapst))
- fix segmentation fault - rollback composer dependencies [\#463](https://github.com/kevinpapst/kimai2/pull/463) ([kevinpapst](https://github.com/kevinpapst))
-  fixed null project for advanced invoice calculator [\#462](https://github.com/kevinpapst/kimai2/pull/462) ([kevinpapst](https://github.com/kevinpapst))
- fix the restart timesheet button [\#436](https://github.com/kevinpapst/kimai2/pull/436) ([kevinpapst](https://github.com/kevinpapst))

**Closed issues:**

- Redirecting when using Kimai on a subdirectory + reverse proxy [\#492](https://github.com/kevinpapst/kimai2/issues/492)
- Installation \(Cannot declare.... in use\) [\#455](https://github.com/kevinpapst/kimai2/issues/455)
- New Number Generator not recognized [\#453](https://github.com/kevinpapst/kimai2/issues/453)
- de/help/invoices returns 404 error [\#452](https://github.com/kevinpapst/kimai2/issues/452)
- Can you Add Brazilian Portuguese Translation? I can help it.. [\#444](https://github.com/kevinpapst/kimai2/issues/444)
- replace all selects with smart-selects and live-search [\#441](https://github.com/kevinpapst/kimai2/issues/441)
- use parsedown-extra for rendering markdown [\#388](https://github.com/kevinpapst/kimai2/issues/388)
- Think about a cooler name [\#133](https://github.com/kevinpapst/kimai2/issues/133)

**Merged pull requests:**

- pagination without reload while keeping filters applied [\#521](https://github.com/kevinpapst/kimai2/pull/521) ([kevinpapst](https://github.com/kevinpapst))
- go back to calendar after editing and creation of time-records [\#519](https://github.com/kevinpapst/kimai2/pull/519) ([kevinpapst](https://github.com/kevinpapst))
- fetch toolbar results without page reload [\#518](https://github.com/kevinpapst/kimai2/pull/518) ([kevinpapst](https://github.com/kevinpapst))
- Form and theme improvements [\#513](https://github.com/kevinpapst/kimai2/pull/513) ([kevinpapst](https://github.com/kevinpapst))
- validation for future and negative times [\#512](https://github.com/kevinpapst/kimai2/pull/512) ([kevinpapst](https://github.com/kevinpapst))
- alphabetical order for selectboxes [\#510](https://github.com/kevinpapst/kimai2/pull/510) ([kevinpapst](https://github.com/kevinpapst))
- Export team timesheets [\#508](https://github.com/kevinpapst/kimai2/pull/508) ([kevinpapst](https://github.com/kevinpapst))
- fix broken sql in activity admin [\#506](https://github.com/kevinpapst/kimai2/pull/506) ([kevinpapst](https://github.com/kevinpapst))
- display invoice entries in ascending order [\#505](https://github.com/kevinpapst/kimai2/pull/505) ([kevinpapst](https://github.com/kevinpapst))
- Improve DOCX template row [\#504](https://github.com/kevinpapst/kimai2/pull/504) ([kevinpapst](https://github.com/kevinpapst))
- do not display admin menu if it has no children [\#500](https://github.com/kevinpapst/kimai2/pull/500) ([kevinpapst](https://github.com/kevinpapst))
- login-screen optimizations [\#493](https://github.com/kevinpapst/kimai2/pull/493) ([lduer](https://github.com/lduer))
- preg\_replace for md-file-extensions when rendering correct link… [\#482](https://github.com/kevinpapst/kimai2/pull/482) ([lduer](https://github.com/lduer))
- Better composer install in the docker [\#481](https://github.com/kevinpapst/kimai2/pull/481) ([tobybatch](https://github.com/tobybatch))
- Update dockerfile for https in composer installer [\#478](https://github.com/kevinpapst/kimai2/pull/478) ([scolson](https://github.com/scolson))
- support line breaks in docx [\#466](https://github.com/kevinpapst/kimai2/pull/466) ([kevinpapst](https://github.com/kevinpapst))
- updated README and docu [\#465](https://github.com/kevinpapst/kimai2/pull/465) ([kevinpapst](https://github.com/kevinpapst))
- allow decimals in users hourly rate [\#460](https://github.com/kevinpapst/kimai2/pull/460) ([kevinpapst](https://github.com/kevinpapst))
- updated all composer packages [\#459](https://github.com/kevinpapst/kimai2/pull/459) ([kevinpapst](https://github.com/kevinpapst))
- moved some packages to dev requirements [\#456](https://github.com/kevinpapst/kimai2/pull/456) ([kevinpapst](https://github.com/kevinpapst))
- Added portuguese translations [\#446](https://github.com/kevinpapst/kimai2/pull/446) ([marquesmatheus](https://github.com/marquesmatheus))
- Simplify timesheet edit form if only one customer is existing [\#443](https://github.com/kevinpapst/kimai2/pull/443) ([kevinpapst](https://github.com/kevinpapst))
- added project variables for invoice templates [\#439](https://github.com/kevinpapst/kimai2/pull/439) ([kevinpapst](https://github.com/kevinpapst))
- added configurable permission system [\#424](https://github.com/kevinpapst/kimai2/pull/424) ([kevinpapst](https://github.com/kevinpapst))
- Only one running timesheet: automatically stop others [\#386](https://github.com/kevinpapst/kimai2/pull/386) ([lduer](https://github.com/lduer))
