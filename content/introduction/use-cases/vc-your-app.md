---
title: Version Control Your Application
---

# Problem

* Do your customers want branches and merges in your application? 
* Do your customers want to review changes in your application before they go live? 
* Do you want to add a pull request workflow to your application?
* Do you want to expose audit log functionality in your application?
* Do you want to expose rollback functionality in your application?

# Dolt solves this by…

If you have an application that would benefit from branches, merges, diffs, logs, and human review of changes, you can use Dolt to power that application. Dolt gives you branch, diff, and merge at the database layer. 

Programmatically access git functionality via procedures, system tables, and functions. Programmatic control of git operations combined with the ability to use standard SQL creates the ideal foundation to add version control to your application.

Dolt ships with standard RDBMS tools like replication and backups. Run Dolt with a hot standby and failover just like MySQL or Postgres.

Hosted Dolt is a hosted version of Dolt that works like AWS RDS. Let us worry about operating Dolt in the cloud. Write your application against a cloud endpoint.

In the past applications that needed these features required slowly changing dimension or soft deletes. These approaches are cumbersome and do not support merge. Dolt gives application the full developemnt power of Git.

# Companies Doing This

[Threekit](https://www.threekit.com/), [Network To Code](https://www.networktocode.com/), [FJA](https://www.fja.com/), [Idearoom](https://www.idearoom.com/)

# Case Studies

* [Nautobot by Network To Code](https://www.dolthub.com/blog/2021-11-19-dolt-nautobot/)
* [Turbine](https://www.dolthub.com/blog/2022-08-17-dolt-turbine/)