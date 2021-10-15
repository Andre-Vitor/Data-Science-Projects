# Introduction

# Installation
For windows:
- Go to [this link](https://www.oracle.com/java/technologies/downloads/#jdk17-windows) and select your OS.
- Check if it is installed by typing `java -version` in the command line.
- Add Java to PATH:
  - search for "edit the environment variables"
  - then, click in "Environment Variables"
  - Click in "New", in System variables.
  - JAVA_HOME and  'C:\Program Files (x86)\Java\jdk1.8.0_251'.  or the path you choose to install. Click ok
  - In the User variable, select Path (the Anaconda path) and select New. Add the name as 'PATH' and the path value as ' C:\Program Files (x86)\Java\jdk1.8.0_251\bin', which is your location of Java bin file

## Installing PySpark

- Go to the [Spark homepage](https://spark.apache.org/downloads.html).
- Download the `.tgz` file and extract. 
- Download Winutils from https://github.com/steveloughran/winutils
- Create a new folder "winutils" and inside create another folder "bin". Put the winutils.exe file inside the "bin" folder.
- Create environment variables "hadoop_home"  "C:\winutils"
- Create environment variables "Spark_home"  "C:\spark" (or your own path)
> Finally, double click the 'path' and change the following as done below where a new path is created "%Spark_Home%\bin' is added and click "OK".





# References
https://www.datacamp.com/community/tutorials/installation-of-pyspark
https://towardsdatascience.com/a-project-driven-approach-to-learning-pyspark-4533c85f52b3
https://medium.com/@GalarnykMichael/install-spark-on-windows-pyspark-4498a5d8d66c


mkdir C:\opt\spark

move C:\Users\T-Gamer\Downloads\spark-3.1.2-bin-hadoop2.7.tgz C:\opt\spark\spark-3.1.2-bin-hadoop2.7.tgz

gzip -d spark-3.1.2-bin-hadoop2.7.tgz
tar xvf spark-3.1.2-bin-hadoop2.7.tar

curl -k -L -o winutils.exe https://github.com/steveloughran/winutils/blob/master/hadoop-2.6.0/bin/winutils.exe?raw=true

setx SPARK_HOME C:\opt\spark\spark-3.1.2-bin-hadoop2.7
setx HADOOP_HOME C:\opt\spark\spark-3.1.2-bin-hadoop2.7
setx PYSPARK_DRIVER_PYTHON ipython
setx PYSPARK_DRIVER_PYTHON_OPTS notebook

Add ;C:\opt\spark\spark-3.1.2-bin-hadoop2.7\bin to your path.

pyspark --master local[2]


conda create --name sparkenv
conda activate sparkenv
brew update
brew cask install adoptopenjdk/openjdk/adoptopenjdk8
pip install pyspark
pip install findspark

# Linux
sudo dpkg -i 