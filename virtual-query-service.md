---
layout: page
title: "runQL Virtual Query Service (runSource)"
permalink: /virtual-query-service/
---

# runQL Virtual Query Service (runSource)

## What is the runSource Virtual Query Service?

**runSource** is a Virtual Query Service that acts as a bridge between your database(s) and external services like Metabase, Power BI, and others.

It enables you to:

- Maintain a single source of truth for queries used across multiple external tools.
- Shield your external services from underlying query changes.
- Securely control access to data without exposing real database credentials.

---

## How It Works

When you create a virtual query through runSource:
- It generates a tokenized query endpoint.
- Your external tool (e.g., BI tool) connects through this endpoint instead of directly accessing your database.

If your underlying database schema changes, you only need to update the source query in runQL — **no updates are needed in all your dashboards or apps**!

---

## Example Scenario

Sara is a Data Analyst at ACME Inc.  
She manages 20 dashboards, each showing the top 10 invoices for a selected region.  
Executives review the dashboards every Monday at 3 PM.

### Sara's Original Query:

```sql
SELECT invoiceId, invoiceAmount, customerName
FROM customers
WHERE region = {{location}}
ORDER BY invoiceAmount DESC
LIMIT 10;
```

### Sara's Virtual Query with runSource:

```
SELECT * FROM runQL WHERE runSource='[generatedToken]' AND location=?;
```

### Schema Change

At 2:30 PM, Sara learns that:

- The `customers` table has been renamed to `customerInvoices`.
- The `region` column has been renamed to `customerRegion`.

Without runQL, she would need to manually update all 20 dashboards.  
**With runQL**, she simply updates the source query in one place:

```sql
SELECT invoiceId, invoiceAmount, customerName
FROM customerInvoices
WHERE customerRegion = {{location}}
ORDER BY invoiceAmount DESC
LIMIT 10;
```

✅ All dashboards automatically reflect the update with no extra work!

