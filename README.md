# Fast_Data_Processing_with_Spark2
Learn how to use Spark to process big data at speed and scale for sharper analytics. Put the principles into practice for faster, slicker big data projects.

Chapter 5: Loading and Saving Data in Spark
1.Use SparkContext and RDDs to handle unstructured data.
2.Use SparkSession and Datasets/DataFrames for semi-structured and structured data. As you will see in the later chapters, SparkSession has unified the read from various formats, such as the .csv, .json, .parquet, .jdbc, .orc, and .text files. Moreover, there is a pluggable architecture called DataSource API to access any type of structured data.

Chapter 6: Manipulating Your RDD
1.A broadcast value can be read by all the workers, but an accumulator can be written by all the workers but read only by the driver. 
2.The flatMap function is a useful utility function that allows you to write a function that returns an iterable of the type you want and then flattens the results. A simple example of this is a case where you want to parse all of the data, but some of it fails to parse. The flatMap function outputs an empty list if it fails or a list with its success if it works.

Chapter 7:Spark 2.0 Concepts
1.“What do data scientists want?”

Chapter 9: Foundations of Datasets/DataFrames – The Proverbial Workhorse for DataScientists
1.For Python and R, the class is still DataFrame, but with all the Dataset APIs. So you can think as of it as this: Datasets in Python and R are called DataFrames. The APIs map exactly, so it is easy to keep the mental model straight.
2.In Scala and Java, Datasets are the main interface and there is no DataFrame class.
3.You will still see the name DataFrame, as in DataFrame Reader,DataFrame Writer, and so on. For all practical purposes, the words DataFrame and Dataset are interchangeable. And you will know when the difference matters.
4.A little bit of history: prior to 1.4, SQLContext had lots of data source functions, including JSON. In 1.4, these functions were moved to the pyspark.sql.DataFrameReader class and specifically the read() function. In 2.0, the read() functions are consolidated under the SparkSession class. The read/write framework is also very extensible in 2.0, and we can add support for new data storage formats with the driver classes.
5.There are two types of aggregations: one on column values and the other on subsets of column values, that is, grouped values of some other columns. Full column aggregation functions act on all the values on a column (actually shorthand for the null group by, that is, df.groupBy().agg…); for example, if you want the average sales for the last three years combined, you can use sql.functions.avg("sales"). But if you want the average sales by year, you will need to usesql.functions.groupby("year").agg("sales":"avg").