# Spark
* [spark](https://github.com/soumya-mishra/AI_DS_ML/blob/master/Pyspark.ipynb)
# Pyspark subpackages
- pyspark.sql
- pyspark.streaming
- pyspark.ml
# Open classes 
- SparkContext
- RDD
- SparkConf
- SparkFiles etc
# Pyspark.sql
- pyspark.sql.SparkSession
- pyspark.sql.DataFrame
- pyspark.sql.Column  etc.
# pyspark.sql.SparkSession
spark = SparkSession.builder \
    .master("local") \
    .appName("Word Count") \
    .config("spark.some.config.option", "some-value") \
    .getOrCreate()

# pyspark.sql.DataFrame
- A distributed collection of data grouped into named columns 
- agg
  df.agg({"age": "max"}).collect() \
o/p - [Row(max(age)=5)] \
from pyspark.sql import functions as F \
df.agg(F.min(df.age)).collect() \
o/p -[Row(min(age)=2)]
