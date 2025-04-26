---
layout: page
title: "runQL Virtual Query Service (runSource)"
permalink: /virtual-query-service/
---

## What is runSource?

**runSource** is a Virtual Query Service that bridges your database(s) and external services like Metabase or Power BI.&#8203;:contentReference[oaicite:27]{index=27}

**Benefits:**

- :contentReference[oaicite:28]{index=28}
- :contentReference[oaicite:29]{index=29}
- :contentReference[oaicite:30]{index=30}&#8203;:contentReference[oaicite:31]{index=31}

**Example:**

:contentReference[oaicite:32]{index=32}&#8203;:contentReference[oaicite:33]{index=33}

Original query:

```sql
SELECT invoiceId, invoiceAmount, customerName
FROM customers
WHERE region = {{location}}
ORDER BY invoiceAmount DESC
LIMIT 10;

SELECT * FROM runQL WHERE runSource='[generatedToken]' AND location=?;

---

### 📁 `runsource-powerbi.md`

```markdown
---
layout: page
title: "Using runSource with Power BI"
permalink: /runsource-powerbi/
---

## Integrating runSource with Power BI

1. In Power BI, expand **Advanced Options** to find the required SQL statement.
2. Configure the connection:
   - **Server**: `<HOST_IP_ADDRESS>:3001`
   - **Database**: `runql`
   - **SQL Statement**: `<runSource Query>`
   - **Username**: `<any value>`
   - **Password**: `<any value>`&#8203;:contentReference[oaicite:40]{index=40}
