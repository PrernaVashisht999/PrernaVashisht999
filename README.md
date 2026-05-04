<!-- ================= HEADER ================= -->

<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=0:020617,45:2563EB,100:7C3AED&height=230&section=header&text=Prerna%20Vashisht&fontSize=48&fontColor=ffffff&animation=fadeIn&fontAlignY=38&desc=Data%20Engineer%20%7C%20SQL%20%7C%20Python%20%7C%20PySpark%20%7C%20Databricks&descSize=18&descAlignY=58" />
</p>

<p align="center">
  <img src="https://readme-typing-svg.demolab.com?font=Poppins&weight=700&size=25&duration=2800&pause=900&color=38BDF8&center=true&vCenter=true&width=1000&lines=Data+Engineer;Building+ETL+%26+Data+Pipeline+Projects;SQL+%7C+Python+%7C+PySpark+%7C+Databricks;Transforming+raw+data+into+clean+and+reliable+pipelines" />
</p>

<h1 align="center">Hi, I'm Prerna Vashisht 👋</h1>

<h3 align="center">
Data Engineer | SQL • Python • PySpark • Databricks | Building ETL & Data Pipeline Projects
</h3>

<p align="center">
  <a href="https://www.linkedin.com/in/prernavashisht">
    <img src="https://img.shields.io/badge/LinkedIn-Prerna%20Vashisht-2563EB?style=for-the-badge&logo=linkedin&logoColor=white" />
  </a>
  <a href="https://mail.google.com/mail/?view=cm&fs=1&to=prerna.dataengineer999@gmail.com">
    <img src="https://img.shields.io/badge/Gmail-Contact%20Me-EA4335?style=for-the-badge&logo=gmail&logoColor=white" />
  </a>
</p>

---

<!-- ================= HERO VISUAL ================= -->

<table>
<tr>
<td width="55%">

## 🚀 Data Engineering Portfolio

I build practical **ETL pipelines** and **data engineering projects** using SQL, Python, PySpark, Apache Spark, Spark SQL, and Databricks.

My focus is on converting raw and semi-structured data into clean, reliable, structured datasets using API ingestion, data transformation, schema standardization, and scalable workflow design.

</td>
<td width="45%">

```python
from pyspark.sql import SparkSession
from pyspark.sql.functions import col

spark = SparkSession.builder \
    .appName("ETL_Pipeline") \
    .getOrCreate()

raw_df = spark.read.json("api_response.json")

clean_df = raw_df.dropDuplicates() \
    .filter(col("job_title").isNotNull())

clean_df.write.mode("overwrite") \
    .format("parquet") \
    .save("silver_layer/")
