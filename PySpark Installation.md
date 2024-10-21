# How to Install PySpark in Windows 11
## Step 1 - Install Java
1)  Spark runs on Java 8/11/17, Scala 2.12/2.13, Python 3.7+, and R 3.5+. Python 3.7 support is deprecated as of Spark 3.4.0. Java 8 prior to version 8u362 support is deprecated as of Spark 3.4.0. When using the Scala API, it is necessary for applications to use the same version of Scala that Spark was compiled for. For example, when using Scala 2.13, use Spark compiled for 2.13, and compile code/applications for Scala 2.13 as well.
2)  Download JDK from Orcale Downloads page (you may need to signup and login to Oracle to download JDKs) - https://www.oracle.com/java/technologies/downloads/#java17-windows
3)  Verify the Java installation by checking the version from command prompt
   ![image](https://github.com/user-attachments/assets/a2c65ef1-b5b9-442c-8464-aa2428f20746)

## Step 2- Install Python
1)  Download Python 3.10.11 from https://www.python.org/downloads/release/python-31011/
> The most recent version of Python (Python 3.13.0) is having issues with data frame operations. When I attempted to use the data frame show action to display the dataset, it resulted in an error in the versions listed below.
>    1. Python 3.13.0 
>    2. Python 3.12.7
2) Install Python 3.10.11 and verify the installation by checking teh version from command prompt
![image](https://github.com/user-attachments/assets/14ccc882-9b72-465f-9f55-685190fd88fd)
3) Make sure to add python.exe to environment variable PATH during the instatallation steps. If missed it, then you have to add it manually in environment variables section

## Step 3 - Install PySpark
1) Install pyspark library using pip in command proompt - "pip install pyspark"
![image](https://github.com/user-attachments/assets/3e297e73-16b2-4436-9522-50d0d5078359)

## Step 4 - Install Apache Spark
1) Download the Apache Spark from https://spark.apache.org/downloads.html
![image](https://github.com/user-attachments/assets/04cbf9fe-0ea8-4119-90fa-4b8980cb9e2c)
2) Click spark-3.5.3-bin-hadoop3.tgz link and it opens up new window to download the zip file
![image](https://github.com/user-attachments/assets/9f66720f-254c-45d1-b533-6d97bb9f9b59)
3) Unzip the file and place it in your preferred folder. For Example: C:\Users\santh\OneDrive\Documents\apps\Spark
![image](https://github.com/user-attachments/assets/9c5079aa-d263-481d-98a6-7eb62195cd58)

## Step 5 - Hadoop Windows Libraries
1) Download Hadoop 3.0.0 windows binaries (https://github.com/steveloughran/winutils/blob/master/hadoop-3.0.0/bin/winutils.exe ) and keep it in your local. Download the Hadoop version specific binaries only. For Example: "C:\Users\santh\OneDrive\Documents\apps\Hadoop\bin"
![image](https://github.com/user-attachments/assets/4d1eb500-7e36-4efc-b4d2-56fd41d8d1fd)

## Step 6 - Setup Environment Variables
1. Setup system environment variables as below
   - HADOOP_HOME    — C:\HADOOP
   - SPARK_HOME     — C:\SPARK\spark-3.5.1-bin-hadoop3
   - PYTHONPATH     — %SPARK_HOME%\python;%SPARK_HOME%\python\lib\py4j-0.10.9.7-src.zip;%PYTHONPATH%
   - SPARK_LOCAL_IP — 127.0.0.1
     
![image](https://github.com/user-attachments/assets/6792c633-eeaa-4d23-a126-09cd1ab162de)

![image](https://github.com/user-attachments/assets/d713cf92-a4fa-4734-ba39-d85729ef44f9)

## Step 7 - Spark Shell Execution
1. Run "spark-shell" command in command prompt
![image](https://github.com/user-attachments/assets/24c0b05d-e97f-4c40-959f-dc7a782592c3)
2. Open Spark Web UI (http://view-localhost:4040/jobs/) in your desired browser
   ![image](https://github.com/user-attachments/assets/81f2bdfb-3ed2-4e6c-a2d2-72a1d0badf62)

## Step 8 - Run Notebook from Visual Studio Code
1. Open Visual Studio and create a new Python notebook.
2. When you run the code, Visual Studio may prompt you to trust the source and will require you to install kernels. Follow the instructions provided by the VS Code editor.
![image](https://github.com/user-attachments/assets/8aa71c3b-e190-4c86-ad88-742bf520d5ae)



