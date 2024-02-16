# ShopApp
> System is not finished!
> 
> ShopApp is system of web applications made in python, created to manage with accounts and shop for some web store.
# Technologies and Libraries
- Flask
- SQLAlchemy
- Docker
- Spark
- Etherium Blockchain
# Flask
- Framework is used for accounts, owner, customer and courier applications
# SQLAlchemy
- Used for creating, managing and retrieving data from MySQL database.
# Docker
- Created system with Docker compose.
- System have 2 parts, one for managing accounts and one for managing shop.
- Each system is created from three Docker images
  - MySQL - for database
  - Image for database migrations
  - Image for applications
- Systems are separeted in different networks so it is not possible to access the bases from the outside.
- Docker volume is used for data backup.
# Spark
- Statistics are made in Docker Image shablon that i found on [Big Data Europe GitHub](https://github.com/big-data-europe/docker-spark).
- Spark claster is reading data from base and gives statistics that are required.
- Spark Master server is alo available
- Containers of spark clasters are in system for managing shop.
# System Variables
For Spark image:
```
HADOOP HOME : C:\hadoop\bin\winutils.exe
JAVA_HOME: C:\Program Files\jdk...
```
For python applications that are using pyspark:
```
PYSPARK_DRIVER_PYTHON=jupyter;
PYSPARK_DRIVER_PYTHON_ARGS=notebook;
PYSPARK_PYTHON=python;
PYTHONUNBUFFERED=1
```