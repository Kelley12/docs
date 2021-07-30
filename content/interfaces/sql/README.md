---
title: Dolt SQL
---

# SQL

## Overview

Dolt data repositories are unique in that they arrive capable of running MySQL compatible SQL statements against them. Your Dolt binary can execute SQL against any Dolt repo you have happen to have locally. Existing RDBMS solutions have optimized their on-disk layout to support the needs of physical plan execution. Dolt makes a different set of tradeoffs, instead using a Merkel Tree to support robust version control semantics, and thus portability of the data. The combination of portability, robust version control semantics, and a SQL interface make Dolt a uniquely compelling data format.

### Executing SQL

There are two ways of executing SQL against your data repository. The first is via the `dolt sql` command, which runs SQL queries from your shell, and the second is the sql-server command, which starts a MySQL compatible server you can connect to with any standard database client.

#### dolt sql

Using `dolt sql` you can issue SQL statements against a local data repository directly. Any writes made to the repository will be reflected in the working set, which can be added via `dolt add` and committed via `dolt commit` as per usual.

There are 2 basic modes which the `dolt sql` command operate in. The first is command line query mode where a semicolon delimited list of queries is provided on the command line using the -q parameter. The second is using the Dolt SQL interactive shell which can be started by running the `dolt sql` command without any arguments in a directory containing a Dolt data repository.

View the `dolt sql` command documentation [here](../cli.md#dolt-sql)

#### dolt sql-server

The `dolt sql-server` command will run a MySQL compatible server which clients can execute queries against. This provides a programmatic interface to get data into or out of a Dolt data repository. It can also be used to connect with third party tooling which supports MySQL.

View the `dolt sql-server` command documentation [here](../cli.md#dolt-sql-server) to learn how to configure the server.

### Dolt CLI in SQL

You can operate several of dolt cli commands in the sql layer directly. This is especially useful if you are using sql in the application layer and want to the query a Dolt repository.

You can find full API documentation [here](dolt-sql-functions.md)

### System Tables

Many of Dolt's unique features are accessible via system tables. These tables allow you to query the same information available from various Dolt commands, such as branch information, the commit log, and much more. You can write queries that examine the history of a table, or that select the diff between two commits. See the individual sections below for more details.

* [dolt\_log table](dolt-system-tables.md#dolt_branches)
* [dolt\_branches table](dolt-system-tables.md#dolt_branches)
* [dolt\_docs table](dolt-system-tables.md#dolt_docs)
* [dolt\_diff tables](dolt-system-tables.md#dolt_diff_tablename)
* [dolt\_history tables](dolt-system-tables.md#dolt_history_tablename)
* [dolt\_schemas table](dolt-system-tables.md#dolt_schemas)

### Concurrency

Dolt supports SQL transactions using the standard transaction control
statements: `START TRANSACTION`, `COMMIT`, `ROLLBACK`, and
`SAVEPOINT`. The `@@autocommit` session variable is also supported,
and behaves identically as in MySQL. `@@autocommit` is enabled by
default using the `dolt sql` shell and the MySQL shell, but some other
clients turn it off by default (notably the [Python mysql
connector](https://dev.mysql.com/doc/connector-python/en/connector-python-api-mysqlconnection-autocommit.html).

## Querying non-HEAD revisions of a database

Dolt SQL supports a variant of [SQL 2011](https://en.wikipedia.org/wiki/SQL:2011) syntax to query non-HEAD revisions of a database via the `AS OF` clause:

```sql
SELECT * FROM myTable AS OF 'kfvpgcf8pkd6blnkvv8e0kle8j6lug7a';
SELECT * FROM myTable AS OF 'myBranch';
SELECT * FROM myTable AS OF 'HEAD^2';
SELECT * FROM myTable AS OF TIMESTAMP('2020-01-01');
SELECT * FROM myTable AS OF 'myBranch' JOIN myTable AS OF 'yourBranch' AS foo;
```

The `AS OF` expression must name a valid Dolt reference, such as a commit hash, branch name, or other reference. Timestamp / date values are also supported. Each table in a query can use a different `AS OF` clause.

In addition to this `AS OF` syntax for `SELECT` statements, Dolt also supports an extension to the standard MySQL syntax to examine the database schema for a previous revision:

```sql
SHOW TABLES AS OF 'kfvpgcf8pkd6blnkvv8e0kle8j6lug7a';
```
