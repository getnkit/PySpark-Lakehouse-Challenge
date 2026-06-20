# References

ไฟล์นี้รวบรวม documentation หลักที่ใช้เป็น reference สำหรับ **PySpark Lakehouse Challenge**

Last reviewed: 2026-06-20

---

## Microsoft Fabric and Lakehouse

กลุ่มนี้คือ reference หลักของ environment ที่ใช้ใน repo เพราะ challenge นี้ใช้ **Microsoft Fabric Notebook + Fabric Lakehouse** เป็น main environment

| Reference | Main use |
|---|---|
| [Data Engineering in Microsoft Fabric documentation](https://learn.microsoft.com/fabric/data-engineering/) | Entry point หลักของ Fabric Data Engineering เช่น Lakehouse, notebooks, Spark job definitions และ feature อื่น ๆ ที่เกี่ยวข้อง |
| [What is a lakehouse in Microsoft Fabric?](https://learn.microsoft.com/fabric/data-engineering/lakehouse-overview) | ใช้ทบทวน Lakehouse concept, OneLake/Lakehouse mental model และการจัดข้อมูลเพื่อ analytics workloads |
| [Lakehouse and Delta Lake tables](https://learn.microsoft.com/fabric/data-engineering/lakehouse-and-delta-tables) | ใช้ดู behavior ของ Fabric Lakehouse table และแนวคิดว่า Lakehouse table ทำงานบน Delta Lake format |
| [Explore Lakehouse data with a notebook](https://learn.microsoft.com/fabric/data-engineering/lakehouse-notebook-explore) | ใช้ทบทวนการทำงานระหว่าง Fabric Notebook กับ attached/default Lakehouse |
| [Load data into a Lakehouse using a notebook](https://learn.microsoft.com/fabric/data-engineering/load-lakehouse-data-into-table) | ใช้เป็น reference เวลาทำตัวอย่าง load data เข้า Lakehouse table จาก notebook |
| [Optimize Delta Lake tables with V-Order](https://learn.microsoft.com/fabric/data-engineering/delta-optimization-and-v-order) | ใช้กับ table optimization, V-Order, OPTIMIZE และ mindset เรื่อง performance บน Fabric |
| [Delta table maintenance in Microsoft Fabric](https://learn.microsoft.com/fabric/data-engineering/lakehouse-table-maintenance) | ใช้ทบทวน table maintenance จาก Fabric UI และ maintenance mindset |
| [VACUUM Delta tables](https://learn.microsoft.com/fabric/data-engineering/delta-lake-vacuum) | ใช้กับ VACUUM behavior, retention, DRY RUN mindset และ cleanup safety |
| [Apache Spark runtimes in Microsoft Fabric](https://learn.microsoft.com/fabric/data-engineering/runtime) | ใช้ดู runtime context, Spark version และข้อควรระวังเรื่อง environment-specific behavior |

---

## Apache Spark and PySpark core

กลุ่มนี้คือ reference หลักของ PySpark syntax และ API ที่ใช้แทบทุกวันใน challenge

| Reference | Main use |
|---|---|
| [Spark SQL, DataFrames and Datasets Guide](https://spark.apache.org/docs/latest/sql-programming-guide.html) | Reference เชิง concept สำหรับ Spark SQL, DataFrame-based structured processing และ mental model ของ Spark SQL |
| [PySpark SQL API reference](https://spark.apache.org/docs/latest/api/python/reference/pyspark.sql/index.html) | API index หลักสำหรับ `SparkSession`, `DataFrame`, `Column`, `DataFrameReader`, `DataFrameWriter`, `Window` และ SQL-related APIs |
| [PySpark DataFrame API](https://spark.apache.org/docs/latest/api/python/reference/pyspark.sql/dataframe.html) | ใช้ตรวจ DataFrame operations เช่น `select`, `filter`, `join`, `groupBy`, `show`, `count`, `explain` และ write methods |
| [PySpark built-in functions](https://spark.apache.org/docs/latest/api/python/reference/pyspark.sql/functions.html) | ใช้กับ `functions as F` เช่น `col`, `lit`, `when`, `to_date`, `regexp_replace`, `sha2`, aggregation functions, window functions, JSON functions และ higher-order functions |
| [PySpark types](https://spark.apache.org/docs/latest/api/python/reference/pyspark.sql/data_types.html) | ใช้กับ `StructType`, `StructField`, `StringType`, `IntegerType`, `DecimalType`, `TimestampType` และ complex types |
| [PySpark Window API](https://spark.apache.org/docs/latest/api/python/reference/pyspark.sql/api/pyspark.sql.Window.html) | ใช้กับ window specification เช่น `partitionBy`, `orderBy` และ pattern เช่น latest record, deduplication, SCD prep |

---

## Spark SQL, performance, and debugging

กลุ่มนี้ใช้กับช่วง performance และ debugging โดยเฉพาะ Day 25-27 และ final pipeline

| Reference | Main use |
|---|---|
| [Spark SQL performance tuning](https://spark.apache.org/docs/latest/sql-performance-tuning.html) | ใช้กับ caching, partition tuning, join strategy, Adaptive Query Execution และ data skew-related performance topics |
| [Spark configuration](https://spark.apache.org/docs/latest/configuration.html) | ใช้เวลาเช็ค runtime/session settings, Spark SQL shuffle partitions หรือ behavior ที่ขึ้นกับ environment |
| [Spark monitoring and instrumentation](https://spark.apache.org/docs/latest/monitoring.html) | ใช้ทบทวน Spark UI, jobs, stages, tasks และ metrics เวลา debug performance |

---

## Structured Streaming

กลุ่มนี้ใช้กับ Day 28-29 และ streaming extension ของ Day 30

| Reference | Main use |
|---|---|
| [Structured Streaming Programming Guide](https://spark.apache.org/docs/latest/streaming/index.html) | Reference หลักสำหรับ streaming DataFrames, micro-batch processing, checkpoints, output modes, sinks และ fault tolerance |
| [PySpark DataStreamReader](https://spark.apache.org/docs/latest/api/python/reference/pyspark.ss/api/pyspark.sql.streaming.DataStreamReader.html) | ใช้ตรวจ syntax และ option ของ `spark.readStream` |
| [PySpark DataStreamWriter](https://spark.apache.org/docs/latest/api/python/reference/pyspark.ss/api/pyspark.sql.streaming.DataStreamWriter.html) | ใช้ตรวจ syntax ของ `.writeStream`, `trigger`, `outputMode`, `option` และ `start` |
| [PySpark StreamingQuery](https://spark.apache.org/docs/latest/api/python/reference/pyspark.ss/api/pyspark.sql.streaming.StreamingQuery.html) | ใช้ดู query lifecycle methods เช่น `start`, `stop`, `awaitTermination`, status และ progress inspection |

---

## Delta Lake concepts

กลุ่มนี้ใช้เป็น concept reference ของ Delta Lake โดยรวม แต่เวลาเอาไปใช้ใน repo นี้ให้ตรวจ Microsoft Fabric docs ควบคู่เสมอ เพราะบาง feature อาจทำงานต่างกันตาม Fabric runtime

| Reference | Main use |
|---|---|
| [Delta Lake documentation](https://docs.delta.io/latest/index.html) | ใช้ทบทวน Delta Lake concepts เช่น transaction log, ACID table behavior, schema enforcement/evolution, time travel, MERGE และ streaming |
| [Delta Lake table batch reads and writes](https://docs.delta.io/latest/delta-batch.html) | ใช้กับ Delta table reads/writes, save modes และ table operations ในภาพรวม |
| [Delta Lake MERGE operation](https://docs.delta.io/latest/delta-update.html) | ใช้กับ update/delete/merge patterns และ upsert mindset |
| [Delta Lake Structured Streaming](https://docs.delta.io/latest/delta-streaming.html) | ใช้ทบทวน Delta tables as streaming sources/sinks ในเชิง concept |