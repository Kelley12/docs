![](../../.gitbook/assets/dolthub-logo.png)

[DoltHub](https://www.dolthub.com) is a place to share Dolt databases. We host public data for free! DoltHub adds a modern, secure, always on database management web GUI to the Dolt ecosystem. Edit your database on the web, have another person review it via a pull request, and have the production database pull it to deploy.

# What is DoltHub

DoltHub is GitHub for Dolt. DoltHub acts as a [Dolt remote](../../concepts/dolt/git/remotes.md) you can [clone, push, pull and fetch](../../reference/cli.md) from. DoltHub adds [permissions](../../concepts/dolthub/permissions.md), [pull requests](../../concepts/dolthub/prs.md), [issues](../../concepts/dolthub/issues.md), and [forks](../../concepts/dolthub/forks.md) to the Dolt ecosystem. Additionally, DoltHub has a modern SQL workbench built in so you can explore and change databases on the web.

# Getting Started

DoltHub has many uses. We recommend getting started by [sharing a database](./data-sharing.md) or participating in a [data bounty](./data-bounties.md).

1. [Data Sharing](./data-sharing.md)

This documentation will walk you through discovering data on DoltHub, cloning a copy locally, making a change on a fork, and submitting a pull request to the original database.

2. [Data Bounties](./data-bounties.md)

DoltHub hosts [Data Bounties](./data-bounties.md) where we pay to have an open database constructed, usually from scraping and transforming public data. This documentation will walk you through step-by-step how to make money contributing to data bounties.

# DoltHub API

DoltHub has [an API](./dolthub-api/README.md) you can script against. The documentation covers:

1. [Authentication](./dolthub-api/authentication.md)
2. [SQL API](./dolthub-api/sql.md) - Used to make read or write SQL queries to a DoltHub database
3. [CSV API](./dolthub-api/csv.md) - Used to download CSV format files of DoltHub tables
4. [Database API](./dolthub-api/database.md) - Used to interact with DoltHub databases and pull requests
5. [Hooks](./dolthub-api/hooks.md) - Used to receive change events to your DoltHub databases

# Guides

- [Transform File Uploads](./transform-uploads.md)

We added a feature to [Transform DoltHub File Uploads](./transform-uploads.md). This allows you to set up an API to receive and transform files that are uploaded to your databases on DoltHub. The transformed files are sent back to DoltHub for import to a DoltHub database.

- [Workspaces](./workspaces.md)

We added the workspaces concept to DoltHub as a staging area for changes made from the
web. Learn what workspaces are and how to use them most effectively.
