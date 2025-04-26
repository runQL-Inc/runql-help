---
layout: page
title: "runQL Virtual Query Service (runSource)"
permalink: /virtual-query-service/
---

# What is the runSource Virtual Query Service?

**runSource** is a bridge between your database and external services like Metabase or Power BI.

## Benefits:
- Single source of truth for shared queries.
- Shields external services from underlying query changes.
- Secures access while hiding database credentials.

## Example

Sara uses a query in her dashboards:

```sql
SELECT invoiceId, invoiceAmount, customerName 
FROM customers 
WHERE region = {{location}} 
ORDER BY invoiceAmount DESC 
LIMIT 10;
