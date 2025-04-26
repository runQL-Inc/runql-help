---
layout: page
title: "Adding Database Connections"
permalink: /adding-database-connections/
---

# Adding Database Connections

Here’s how to connect different database types in runQL:

## BigQuery
1. Create a Service Account and download the JSON key.
2. Go to **Add Connection** > **BigQuery**.
3. Enter project details and upload the key.
4. Test the connection.

## Databricks
1. Generate a Personal Access Token.
2. Find the cluster host and path under JDBC/ODBC.
3. Go to **Add Connection** > **Databricks**.
4. Enter details and test.

## MSSQL
1. Gather server address, port, username, password.
2. Go to **Add Connection** > **MSSQL**.
3. Test connection.

## MongoDB
1. Obtain connection URI.
2. Go to **Add Connection** > **MongoDB**.
3. Test connection.

## MySQL
1. Gather server address, port, database, username, password.
2. SSL/SSH optional.
3. Go to **Add Connection** > **MySQL**.
4. Test connection.

## Neo4j
1. Gather host, port, db name, username, password.
2. Go to **Add Connection** > **Neo4j**.
3. Test connection.

## Oracle
1. Gather host, port, service/SID, username, password.
2. Install Oracle Client if needed.
3. Go to **Add Connection** > **Oracle**.
4. Test connection.

## Postgres
1. Gather host, port, db name, username, password.
2. Go to **Add Connection** > **Postgres**.
3. Test connection.

## Redshift
1. Gather cluster endpoint, port, db name, username, password.
2. Go to **Add Connection** > **Redshift**.
3. Test connection.

## Snowflake
1. Gather account ID, username, password, role, warehouse.
2. Go to **Add Connection** > **Snowflake**.
3. Test connection.

## Trino
1. Gather coordinator host, port, catalog, schema.
2. Go to **Add Connection** > **Trino**.
3. Test connection.
