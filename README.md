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