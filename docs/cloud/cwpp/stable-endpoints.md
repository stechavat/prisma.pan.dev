---
id: stable-endpoints
title: Stable Endpoints
sidebar_label: Stable Endpoints
---

API calls are essential in developing automation scripts for reporting, deployment and config-as-code scenarios.
Keeping that in mind, we strive to maintain API calls over versions and avoid breaking changes unless absolutely necessary because of introduction of new features or enhancements.
While we realize this need for stability for such API endpoints, as new features get added, sometimes the need for additional fields becomes a must. 
Hence to balance the need, for the following endpoints, we will only introduce changes when absolutely necessary and indicate these changes as part of "Breaking Changes" section of the version Release Notes so that users are aware prior to upgrading. 

For Compute SAAS (Prisma Cloud Enterprise Edition) customers, we will publish upgrade plan including date of upgrade, link to release notes with breaking changes notifications [here](https://docs.twistlock.com/docs/enterprise_edition/welcome/announcements.html).
Additionally, email notification will also be sent to SaaS customers, prior to upgrade in order to prepare for the upgrade with changes needed.


## Reporting Endpoints

Reporting API calls are the ones used to download health or scan data such as vulnerabilities/compliance/runtime.   
Access to the underlying data in JSON and CSV formats allows customers to easily access & transform data into business intelligence in the forms that meet their needs.  
The output may be human-readable reports or, in other cases, the reporting data may feed automated decisions & processes.

These are mostly under **Monitor** section in Compute:

* `/registry`
* `/containers`
* `/images`
* `/incidents`
* `/scans`
  - `type=ciServerless`
  - `type=ciImage`
* `/hosts`
* `/stats/vulnerabilities`
* `/stats/compliance`


## Config as Code

"Configuration as code is the formal migration of config between environments, backed by a version control system."  
Customers who want to programmatically store and manage the configuration of infrastructure components, can utilize these to automate these components using the same approaches that they've used for production code & services. 

Key C-as-C endpoints:

* `/policies`
  - `/runtime/container`
  - `/runtime/host`
  - `/runtime/serverless`
  - `/vulnerability/images`
  - `/vulnerability/ci/images`
  - `/vulnerability/vms`
  - `/vulnerability/serverless`
  - `/compliance`
* `/settings`
  - `/registry`
* `/collections`


## Deployment & Config

Deployment and config endpoints are essential for properly being able to automate the installation of the console, defenders, as well as any configuration that deals with integrations.  
These are useful to those who base their management of environments on automation, using tools such as Ansible, Puppet, Terraform etc to define desired configurations.

Key deployment and config endpoints:
  
* `/users`
* `/version`
* `/authenticate-client`
* `/authenticate`
* `/util/twistcli`
* `/defenders`
* `/_ping`

