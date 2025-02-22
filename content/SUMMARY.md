# Table of contents

## Introduction

- [What Is Dolt?](introduction/what-is-dolt.md)
- [Installation](introduction/installation.md)
  - [Linux](introduction/installation/linux.md)
  - [Windows](introduction/installation/windows.md)
  - [Mac](introduction/installation/mac.md)
  - [Build from Source](introduction/installation/source.md)
  - [Application Server](introduction/installation/application-server.md)
  - [Docker](introduction/installation/docker.md)
  - [Upgrading](introduction/installation/upgrading.md)
- [Getting Started](introduction/getting-started.md)
  - [Version Controlled Database](introduction/getting-started/database.md)
  - [Git For Data](introduction/getting-started/git-for-data.md)
  - [Versioned MySQL Replica](introduction/getting-started/versioned-mysql-replica.md)
- [Use Cases](introduction/use-cases.md)
  - [Data Sharing](introduction/use-cases/data-sharing.md)
  - [Data and Model Quality Control](introduction/use-cases/data-and-model-quality.md)
  - [Manual Data Curation](introduction/use-cases/manual-data-curation.md)
  - [Version Control for your Application](introduction/use-cases/vc-your-app.md)
  - [Versioned MySQL Replica](introduction/use-cases/versioned-replica.md)
  - [Audit](introduction/use-cases/audit.md) 
  - [Configuration Management](introduction/use-cases/configuration-management.md)
  - [Offline First](introduction/use-cases/offline-first.md)

## Concepts

- [Dolt](concepts/dolt.md)
  - [Git](concepts/dolt/git/README.md)
    - [Commits](concepts/dolt/git/commits.md)
    - [Log](concepts/dolt/git/log.md)
    - [Diff](concepts/dolt/git/diff.md)
    - [Branch](concepts/dolt/git/branch.md)
    - [Merge](concepts/dolt/git/merge.md)
    - [Conflicts](concepts/dolt/git/conflicts.md)
    - [Remotes](concepts/dolt/git/remotes.md)
    - [Working Set](concepts/dolt/git/working-set.md)
  - [SQL](concepts/dolt/sql/README.md)
    - [Databases](concepts/dolt/sql/databases.md)
    - [Schema](concepts/dolt/sql/schema.md)
    - [Tables](concepts/dolt/sql/table.md)
    - [Primary Keys](concepts/dolt/sql/primary-key.md)
    - [Types](concepts/dolt/sql/types.md)
    - [Indexes](concepts/dolt/sql/indexes.md)
    - [Views](concepts/dolt/sql/views.md)
    - [Constraints](concepts/dolt/sql/constraints.md)
    - [Triggers](concepts/dolt/sql/triggers.md)
    - [Procedures](concepts/dolt/sql/procedures.md)
    - [Users/Grants](concepts/dolt/sql/users-grants.md)
    - [Transactions](concepts/dolt/sql/transaction.md)
    - [System Variables](concepts/dolt/sql/system-variables.md)
  - [RDBMS](concepts/dolt/rdbms/README.md)
    - [Server](concepts/dolt/rdbms/server.md)
    - [Backups](concepts/dolt/rdbms/backups.md)
    - [Replication](concepts/dolt/rdbms/replication.md)
- [DoltHub/DoltLab](concepts/dolthub.md)
  - [Permissions](concepts/dolthub/permissions.md)
  - [Pull Requests](concepts/dolthub/prs.md)
  - [Issues](concepts/dolthub/issues.md)
  - [Forks](concepts/dolthub/forks.md)

## Products

- [Hosted Dolt](products/hosted/README.md)
  - [Getting Started](products/hosted/getting-started.md)
  - [Notable Features](products/hosted/notable-features.md)
  - [SQL Workbench](products/hosted/sql-workbench.md)
  - [Cloning a Hosted Database](products/hosted/cloning.md)
  - [Using DoltHub as a Remote](products/hosted/dolthub-as-remote.md)
  - [Infrastructure](products/hosted/infrastructure.md)
- [DoltHub](products/dolthub/README.md)
  - [Data Sharing](products/dolthub/data-sharing.md)
  - [Data Bounties](products/dolthub/data-bounties.md)
  - [DoltHub API](products/dolthub/dolthub-api/README.md)
    - [Authentication](products/dolthub/dolthub-api/authentication.md)
    - [SQL](products/dolthub/dolthub-api/sql.md)
    - [CSV](products/dolthub/dolthub-api/csv.md)
    - [Database](products/dolthub/dolthub-api/database.md)
    - [Hooks](products/dolthub/dolthub-api/hooks.md)
  - [Transform File Uploads](products/dolthub/transform-uploads.md)
  - [Workspaces](products/dolthub/workspaces.md)
- [DoltLab](products/doltlab/README.md)
  - [Install DoltLab](products/doltlab/installation.md)
  - [Administrator Guide](products/doltlab/administrator.md)

## SQL Reference

- [Running the Server](reference/sql/server/README.md)
  - [Configuration](reference/sql/server/configuration.md)
  - [Access Management](reference/sql/server/access-management.md)
  - [Branch Permissions](reference/sql/server/branch-permissions.md)
  - [Backups](reference/sql/server/backups.md)
  - [Replication](reference/sql/server/replication.md)
  - [Garbage Collection](reference/sql/server/garbage-collection.md)
  - [Troubleshooting](reference/sql/server/troubleshooting.md)
- [Version Control Features](reference/sql/version-control/README.md)
  - [Using Branches](reference/sql/version-control/branches.md)
  - [Merges](reference/sql/version-control/merges.md)
  - [Querying History](reference/sql/version-control/querying-history.md)
  - [Using Remotes](reference/sql/version-control/remotes.md)
  - [Procedures](reference/sql/version-control/dolt-sql-procedures.md)
  - [Functions](reference/sql/version-control/dolt-sql-functions.md)
  - [System Tables](reference/sql/version-control/dolt-system-tables.md)
  - [System Variables](reference/sql/version-control/dolt-sysvars.md)
  - [Saved Queries](reference/sql/version-control/saved-queries.md)
- [SQL Language Support](reference/sql/sql-support/README.md)
  - [Data Description](reference/sql/sql-support/data-description.md)
  - [Expressions, Functions, Operators](reference/sql/sql-support/expressions-functions-operators.md)
  - [Supported Statements](reference/sql/sql-support/supported-statements.md)
  - [MySQL Information Schema](reference/sql/sql-support/information-schema.md)
  - [Miscellaneous](reference/sql/sql-support/miscellaneous.md)
- [Supported Clients](reference/sql/supported-clients/README.md)
  - [Programmatic](reference/sql/supported-clients/clients.md)
  - [SQL Editors](reference/sql/supported-clients/sql-editors.md)
  - [Spreadsheets](reference/sql/supported-clients/spreadsheets.md)
- [Benchmarks and Metrics](reference/sql/benchmarks/README.md)
  - [Correctness](reference/sql/benchmarks/correctness.md)
  - [Latency](reference/sql/benchmarks/latency.md)
  - [Import](reference/sql/benchmarks/import.md)

## CLI Reference

- [CLI Command Reference](reference/cli.md)

## Architecture

- [Overview](architecture/architecture.md)
- [Storage Engine](architecture/storage-engine.md)
  - [Prolly Trees](architecture/storage-engine/prolly-tree.md)
- [SQL](architecture/sql.md)
  - [Go MySQL Server](architecture/sql/go-mysql-server.md)
  - [Vitess](architecture/sql/vitess.md)

## Guides

- [Contributing](guides/contributing.md)
  - [dolt](guides/contributing/dolt.md)
  - [go-mysql-server](guides/contributing/go-mysql-server.md)
- [MySQL to Dolt Replication](guides/binlog-replication.md)
- [Importing Data](guides/import.md)

## Other

- [FAQ](other/faq.md)
- [Roadmap](other/roadmap.md)
- [Versioning](other/versioning.md)
