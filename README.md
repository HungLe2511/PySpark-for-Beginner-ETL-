# PySpark-for-Beginner-ETL

! This project is built using Linux operating system (ubuntu 22.04)

This document is designed to be read in parallel with the code in the `PySpark-for-Beginner-ETL` repository. Together, these constitute what we consider to be a 'best practices' approach to writing ETL jobs using Apache Spark and its Python ('PySpark') APIs. This project addresses the following topics:

- set up environment, var environment;
- Resilient Distributed Datasets(RDD), Data Frame(DF), Spark SQL;
- Spark architechture;
- how to pass configuration parameters to a PySpark job;
- how to handle dependencies on other modules and packages; and,
- what constitutes a 'meaningful' test for an ETL job.

## Set up environment, var environment

Install java 11
```sh
sudo apt-get install openjdk-11-jdk
```

Install python 3.10
```sh
sudo apt install python3.10
```

Install spark (should install the full version of spark to use it, the version you install with `pip install pyspark` will be difficult to understand). After downloaded, install it
```sh
wget https://dlcdn.apache.org/spark/spark-3.5.1/spark-3.5.1-bin-hadoop3.tgz
tar -xzvf spark-3.5.1-bin-hadoop3.tgz
```

Set up variable environment, open file .bashrc by 
```sh
# open file
nano ~/.bashrc

# save config
source ~/.bashrc
```

and add
```sh
export SPARK_HOME=/path/to/spark
export PATH=$PATH:$SPARK_HOME/bin
```
## Resilient Distributed Datasets(RDD), Data Frame(DF), Spark SQL

![Codespace](image/RDD_DF_2.png)







## Spark architechture
The system currently supports several cluster managers:

- Standalone — a simple cluster manager included with Spark that makes it easy to set up a cluster.
  
![Codespace](image/Standalone-Cluster.webp)

  
- Apache Mesos — a general cluster manager that can also run Hadoop MapReduce and service applications.

![Codespace](image/Apache-Mesos.png)


- Hadoop YARN — the resource manager in Hadoop 2.

![Codespace](image/yarn_arch.webp)
- Kubernetes — an open-source system for automating deployment, scaling, and management of containerized applications.

![Codespace](image/1_FIuvzHDPvibv6fV-2qdLrQ.webp)
