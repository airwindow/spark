# Dive into Original Spark Source Code.
Original source code to look into
https://github.com/apache/spark/tree/5b021ce0990ec675afc6939cc2c06f041c973d17/core/src/main/scala/spark

# Some useful notes.
https://github.com/JerryLead/SparkInternals

# Introduction to AmpLab Spark Internals - Matei Zaharia (Databricks)
https://www.youtube.com/watch?v=49Hr5xZyTEA

# A Deeper Understanding of Spark Internals - Aaron Davidson (Databricks)
https://www.youtube.com/watch?v=dmL0N3qfSc8

# Interesting code & docs to look into
The collaboration between Job and Mesos
https://github.com/apache/spark/blob/5b021ce0990ec675afc6939cc2c06f041c973d17/core/src/main/scala/spark/Executor.scala
https://github.com/apache/spark/blob/5b021ce0990ec675afc6939cc2c06f041c973d17/core/src/main/scala/spark/SimpleJob.scala
https://hadoop.apache.org/docs/stable/hadoop-mapreduce-client/hadoop-mapreduce-client-app/apidocs/org/apache/hadoop/mapreduce/v2/app/webapp/dao/TasksInfo.html
http://mesos.apache.org/api/latest/java/org/apache/mesos/Executor.html
http://mesos.apache.org/api/latest/java/org/apache/mesos/Protos.TaskStatus.html


Schedulers


https://github.com/rohgar/scala-spark-4/wiki/Wide-vs-Narrow-Dependencies
https://github.com/apache/spark/blob/5b021ce0990ec675afc6939cc2c06f041c973d17/core/src/main/scala/spark/Scheduler.scala
https://github.com/apache/spark/blob/5b021ce0990ec675afc6939cc2c06f041c973d17/core/src/main/scala/spark/DAGScheduler.scala
https://github.com/apache/spark/blob/5b021ce0990ec675afc6939cc2c06f041c973d17/core/src/main/scala/spark/LocalScheduler.scala#L33


MesoScheduler


http://mesos.apache.org/documentation/latest/architecture/
http://mesos.apache.org/api/latest/java/org/apache/mesos/MesosSchedulerDriver.html
http://mesos.apache.org/api/latest/java/org/apache/mesos/Scheduler.html
https://github.com/apache/spark/blob/5b021ce0990ec675afc6939cc2c06f041c973d17/core/src/main/scala/spark/MesosScheduler.scala#L203


Fetcher(Pull Model)
https://github.com/apache/spark/blob/5b021ce0990ec675afc6939cc2c06f041c973d17/core/src/main/scala/spark/ShuffleManager.scala#L71
https://github.com/apache/spark/blob/5b021ce0990ec675afc6939cc2c06f041c973d17/core/src/main/scala/spark/ShuffleMapTask.scala#L29
https://github.com/apache/spark/blob/5b021ce0990ec675afc6939cc2c06f041c973d17/core/src/main/scala/spark/MapOutputTracker.scala#L46
https://github.com/apache/spark/blob/5b021ce0990ec675afc6939cc2c06f041c973d17/core/src/main/scala/spark/MapOutputTracker.scala#L22
https://github.com/apache/spark/blob/5b021ce0990ec675afc6939cc2c06f041c973d17/core/src/main/scala/spark/ShuffleFetcher.scala
https://github.com/apache/spark/blob/5b021ce0990ec675afc6939cc2c06f041c973d17/core/src/main/scala/spark/SimpleShuffleFetcher.scala#L16


ShuffleDependency
https://github.com/apache/spark/blob/5b021ce0990ec675afc6939cc2c06f041c973d17/core/src/main/scala/spark/SparkContext.scala#L316
https://github.com/apache/spark/blob/5b021ce0990ec675afc6939cc2c06f041c973d17/core/src/main/scala/spark/PairRDDFunctions.scala#L58
https://github.com/apache/spark/blob/5b021ce0990ec675afc6939cc2c06f041c973d17/core/src/main/scala/spark/ShuffledRDD.scala#L39
https://github.com/apache/spark/blob/5b021ce0990ec675afc6939cc2c06f041c973d17/core/src/main/scala/spark/ShuffleMapTask.scala#L40
https://github.com/apache/spark/blob/5b021ce0990ec675afc6939cc2c06f041c973d17/core/src/main/scala/spark/MapOutputTracker.scala#L14
https://github.com/apache/spark/blob/5b021ce0990ec675afc6939cc2c06f041c973d17/core/src/main/scala/spark/Dependency.scala


ShuffleRDD LifeCycle
https://github.com/apache/spark/blob/5b021ce0990ec675afc6939cc2c06f041c973d17/core/src/main/scala/spark/PairRDDFunctions.scala#L63
https://github.com/apache/spark/blob/5b021ce0990ec675afc6939cc2c06f041c973d17/core/src/main/scala/spark/Dependency.scala#L10
https://github.com/apache/spark/blob/5b021ce0990ec675afc6939cc2c06f041c973d17/core/src/main/scala/spark/ShuffledRDD.scala#L25
https://github.com/apache/spark/blob/5b021ce0990ec675afc6939cc2c06f041c973d17/core/src/main/scala/spark/DAGScheduler.scala#L153
note: only ShuffleDep causes the add of new stage
https://github.com/apache/spark/blob/5b021ce0990ec675afc6939cc2c06f041c973d17/core/src/main/scala/spark/DAGScheduler.scala#L130


Transformations & RDD
https://github.com/apache/spark/blob/5b021ce0990ec675afc6939cc2c06f041c973d17/core/src/main/scala/spark/RDD.scala#L89
https://github.com/apache/spark/blob/5b021ce0990ec675afc6939cc2c06f041c973d17/core/src/main/scala/spark/RDD.scala#L290
https://www.scala-lang.org/api/current/scala/collection/Iterator.html
https://github.com/apache/spark/blob/5b021ce0990ec675afc6939cc2c06f041c973d17/core/src/main/scala/spark/RDD.scala#L74



