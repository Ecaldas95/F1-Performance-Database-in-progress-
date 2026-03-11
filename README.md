# 🏎️ F1 Performance & Statistics Database (2025)

### Project Overview
This project consists of a relational database designed to manage and analyze Formula 1 racing data. It was built to practice complex SQL operations, data structuring, and performance monitoring—skills directly applicable to operational analysis and live data environments.

### Technical Specs
* **Language:** SQL (MySQL)
* **Key Features:** Relational schema, automated data dumps, and advanced querying (Joins, Aggregations, Group By).
* **Data Volume:** +600 records across multiple racing entities.

### Sample Query: Driver Reliability (DNF Analysis)
One of the key metrics tracked is the "Did Not Finish" (DNF) count per driver to assess mechanical or driver-related consistency.

```sql
SELECT driver_name, COUNT(*) as dnf_count
FROM results
WHERE status = 'DNF'
GROUP BY driver_name
ORDER BY dnf_count DESC;
