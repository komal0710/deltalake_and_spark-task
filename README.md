# deltalake_and_spark-task
## Understanding of Deltalake
Delta Lake is a project that was developed by Databricks. Delta Lake is an open source storage layer that sits on top of the Apache Spark services which brings reliability to data lakes. Delta Lake provides a new feature which includes ACID transactions, scalable metadata handling, and unifies streaming and batch data processing. Delta Lake runs on top of your existing data lake and is fully compatible with Apache Spark APIs.

## What is Apache Spark?
Apache Spark is a lightning-fast cluster computing technology, designed for fast computation. It is based on Hadoop MapReduce and it extends the MapReduce model to efficiently use it for more types of computations, which includes interactive queries and stream processing. The main feature of Spark is its in-memory cluster computing that increases the processing speed of an application.

Spark is designed to cover a wide range of workloads such as batch applications, iterative algorithms, interactive queries and streaming. Apart from supporting all these workload in a respective system, it reduces the management burden of maintaining separate tools.

How Deltalake and Apache Spark works together?
Delta lake provides a storage layer on top of existing cloud storage data lake. It acts as a middle layer between Spark runtime and cloud storage. When you store data as delta table by default data is stored as parquet file in your cloud storage.
Delta Lake will generate delta logs for each committed transactions. Delta logs will have delta files stored as JSON which has information about the operations occurred and details about the latest snapshot of the file and also it contains the information about the statistics of the data. Delta files are sequentially increasing named JSON files and together make up the log of all changes that have occurred to a table. Delta Lake is only, the open source version of Delta Lake is only two months old. And so what we’re doing is we are working hard to open source all of the different APIs that exist. So update, delete, merge, history, all of those kinds of things that you can do inside of Databricks will also be available in the open source version.

Set up Apache Spark with Delta Lake
Follow these instructions to set up Delta Lake with Spark. You can run the steps in this guide on your local machine in the following two ways:
1.	Run interactively: Start the Spark shell (Scala or Python) with Delta Lake and run the code snippets interactively in the shell.
2.	Run as a project: Set up a Maven or SBT project (Scala or Java) with Delta Lake, copy the code snippets into a source file, and run the project.


