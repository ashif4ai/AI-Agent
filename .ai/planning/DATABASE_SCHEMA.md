# Database Schema

## Database Information
- **Type:** [Relational / NoSQL / Graph]
- **Technology:** [PostgreSQL / MongoDB / etc.]
- **Version:** [X.Y.Z]
- **Last Updated:** [YYYY-MM-DD]

---

## Entity Relationship Diagram

```
[ASCII ER Diagram or reference to external diagram]
```

---

## Core Tables/Collections

### Table 1: [Table Name]
**Purpose:** [What this table stores]

| Column | Type | Nullable | Default | Constraints | Notes |
|--------|------|----------|---------|-------------|-------|
| id | INT | No | SERIAL | PRIMARY KEY | Auto-incrementing ID |
| [field] | [type] | [Yes/No] | [value] | [constraints] | [notes] |

**Indexes:**
- Primary key on `id`
- Index on `[field]` for [reason]

**Sample Data:**
```json
{
  "id": 1,
  "field": "value"
}
```

---

### Table 2: [Table Name]
[Repeat structure above]

---

## Relationships

### One-to-Many: [Table1] → [Table2]
```
Table1.id → Table2.table1_id
```
- Cascade delete: [Yes/No]
- Cascade update: [Yes/No]

### Many-to-Many: [Table1] ↔ [Table2]
**Junction Table:** [table_name]

| Column | Type | Constraints |
|--------|------|-------------|
| table1_id | INT | FOREIGN KEY |
| table2_id | INT | FOREIGN KEY |

---

## Views (if applicable)

### View 1: [View Name]
**Purpose:** [What this view provides]

```sql
CREATE VIEW view_name AS
SELECT ...
```

---

## Stored Procedures (if applicable)

### Procedure 1: [Procedure Name]
**Purpose:** [What it does]

```sql
CREATE PROCEDURE procedure_name
AS BEGIN
  ...
END
```

---

## Migrations

### Migration 1: [Description]
- **Date:** [YYYY-MM-DD]
- **Version:** [X.X]
- **Status:** [Pending / Applied]

```sql
-- Up
ALTER TABLE table_name ADD COLUMN new_column VARCHAR(255);

-- Down
ALTER TABLE table_name DROP COLUMN new_column;
```

### Migration 2: [Description]
[Repeat structure]

---

## Constraints & Rules

### Not Null Constraints
- `table.field`: [Reason]

### Unique Constraints
- `table.field`: [Reason]

### Check Constraints
- `table`: [Constraint expression]

### Business Rules
1. [Rule 1]
2. [Rule 2]

---

## Indexing Strategy

### Primary Indexes
| Table | Column | Type | Reason |
|-------|--------|------|--------|
| [table] | [column] | UNIQUE | [Why indexed] |

### Performance Indexes
| Table | Column | Type | Reason |
|-------|--------|------|--------|
| [table] | [column] | B-TREE | [Why indexed] |

### Composite Indexes
| Table | Columns | Reason |
|-------|---------|--------|
| [table] | [col1], [col2] | [Why composite] |

---

## Partitioning Strategy (if applicable)

### Partition 1: [Name]
- **Strategy:** [By date / By range / By hash]
- **Key:** [Column]
- **Retention:** [Duration]

---

## Backup & Recovery

### Backup Schedule
- **Frequency:** [Daily / Weekly / Real-time]
- **Type:** [Full / Incremental / Differential]
- **Storage:** [Location]
- **Retention:** [Duration]

### Recovery Procedures
1. [RTO target]
2. [RPO target]
3. [Recovery steps]

---

## Performance Tuning

### Query Optimization
- [Optimization 1]
- [Optimization 2]

### Cache Strategy
- [Caching approach]

### Archive Strategy
- [Old data handling]

---

## Data Dictionary

### [Field Name]
- **Table:** [Table]
- **Type:** [Data type]
- **Format:** [If applicable]
- **Valid Values:** [If applicable]
- **Description:** [What it stores]

---

## Security & Access Control

### Data Classification
- **Public:** [Fields]
- **Internal:** [Fields]
- **Sensitive:** [Fields]
- **Restricted:** [Fields]

### Access Controls
- **Role:** [Role name]
  - **Permissions:** [Select / Insert / Update / Delete]
  - **Tables:** [Which tables]

---

## Future Considerations

### Planned Changes
- [Change 1]
- [Change 2]

### Scaling Considerations
- [Sharding strategy]
- [Replication setup]

---

**Database Administrator:** [Name]
**Last Reviewed:** [YYYY-MM-DD]
**Next Review:** [YYYY-MM-DD]
