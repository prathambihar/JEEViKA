`--packages` option, examples:
    ```bash
   spark-shell --packages Azure:mmlspark:0.12
   pyspark --packages Azure:mmlspark:0.12
   spark-submit --packages Azure:mmlspark:0.12 MyApp.jar
   spark-shell --packages Azure:mmlspark:0.13
   pyspark --packages Azure:mmlspark:0.13
   spark-submit --packages Azure:mmlspark:0.13 MyApp.jar
   ```
 This can be used in other Spark contexts too, for example, you can use MMLSpark
@@ -156,7 +156,7 @@ the above example, or from python:
   ```python
   import pyspark
   spark = pyspark.sql.SparkSession.builder.appName("MyApp") \
               .config("spark.jars.packages", "Azure:mmlspark:0.12") \
               .config("spark.jars.packages", "Azure:mmlspark:0.13") \
               .getOrCreate()
   import mmlspark
   ```
@@ -172,7 +172,7 @@ running script actions, see [this
guide](https://docs.microsoft.com/en-us/azure/hdinsight/hdinsight-hadoop-customize-cluster-linux#use-a-script-action-during-cluster-creation).
 The script action url is:
<https://mmlspark.azureedge.net/buildartifacts/0.12/install-mmlspark.sh>.
<https://mmlspark.azureedge.net/buildartifacts/0.13/install-mmlspark.sh>.
 If you're using the Azure Portal to run the script action, go to `Script
actions` → `Submit new` in the `Overview` section of your cluster blade.  In
@@ -188,7 +188,7 @@ cloud](http://community.cloud.databricks.com), create a new [library from Maven
coordinates](https://docs.databricks.com/user-guide/libraries.html#libraries-from-maven-pypi-or-spark-packages)
in your workspace.
 For the coordinates use: `Azure:mmlspark:0.12`.  Ensure this library is
For the coordinates use: `Azure:mmlspark:0.13`.  Ensure this library is
attached to all clusters you create.
 Finally, ensure that your Spark cluster has at least Spark 2.1 and Scala 2.11.
@@ -202,7 +202,7 @@ your `build.sbt`:
    ```scala
   resolvers += "MMLSpark Repo" at "https://mmlspark.azureedge.net/maven"
   libraryDependencies += "com.microsoft.ml.spark" %% "mmlspark" % "0.12"
   libraryDependencies += "com.microsoft.ml.spark" %% "mmlspark" % "0.13"
   ```
 ### Building from source
