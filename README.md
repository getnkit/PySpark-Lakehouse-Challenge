# PySpark Lakehouse Challenge

Repo นี้เป็น 30-day hands-on learning lab สำหรับฝึก **PySpark**, ทำความเข้าใจ **Spark execution concepts** และสร้างพื้นฐานการทำงานกับ **Lakehouse pipeline patterns** ด้วย **Microsoft Fabric Notebook** และ **Microsoft Fabric Lakehouse**

เนื้อหาเน้นการลงมือทำจริงผ่าน daily notebooks ตั้งแต่ PySpark พื้นฐาน, DataFrame transformations, Delta/Lakehouse table operations, data quality checks, incremental processing, performance debugging ไปจนถึง Structured Streaming และ final mini Lakehouse pipeline

---

## What this repo covers

- PySpark DataFrame API
- Schema, read/write และ explicit schema handling
- Column operations, cleansing, joins, aggregations และ window functions
- Spark SQL และ temporary views
- Nested JSON และ complex data types
- Delta / Lakehouse table concepts
- Append, overwrite, partitioning, MERGE, schema drift, time travel และ table maintenance
- Bronze, Silver, Gold pipeline patterns
- Data quality checks และ quarantine tables
- Incremental load, watermark และ idempotency
- SCD Type 1 และ Type 2 basics
- Shuffle, broadcast join, data skew, cache/persist และ `explain()`
- Structured Streaming basics และ Lakehouse streaming pattern
- Final mini Lakehouse pipeline

---

## Repository structure

```text
pyspark-lakehouse-challenge/
├── diagrams/     # Mermaid diagrams and technical infographics
├── docs/         # Reference documentation
├── notebooks/    # Daily Fabric notebooks
├── sample_data/  # Small mock/sample data used in selected notebooks
└── README.md
```

---

## Learning path

| Phase | Focus |
|---|---|
| Phase 1 | Spark foundation และ PySpark core |
| Phase 2 | PySpark transformation skills |
| Phase 3 | Lakehouse และ Delta table concepts |
| Phase 4 | Production-style Lakehouse pipeline patterns |
| Phase 5 | Performance debugging, Structured Streaming และ final pipeline |

---

## How to use this repo

เปิด notebook ตามลำดับจาก `notebooks/day_01_...ipynb` ถึง `notebooks/day_30_...ipynb`

แต่ละ notebook โดยทั่วไปจะมี:

- Goal of the day
- Why it matters in production
- Key concepts
- Concept explanation
- PySpark examples
- Exercises
- Common mistakes
- Expected output / success criteria
- Final takeaway

Notebook ถูกออกแบบให้รันใน **Microsoft Fabric Notebook** โดย attach กับ **Fabric Lakehouse**

---

## References

เอกสารอ้างอิงหลักที่ใช้ตลอด challenge อยู่ที่:

```text
docs/references.md
```