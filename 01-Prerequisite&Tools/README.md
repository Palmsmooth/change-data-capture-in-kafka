# Prerequisite&Tools
## Step 1: Provision a Cloud SQL
### Create Cloud SQL
- kafka-class-db-001 is the source that contains the actual data
- kafka-class-db-002 is the target database waiting for data to be delivered by the sink connector

<img src="image\provision cloud sql.png" width="100%" height="40%">

### Using Cluod Shell in Cloud SQL

- click kafka-class-db-001

<img src="image\kafka-class-db-001.png" width="100%" height="40%">

- a user can be created

<img src="image\create user.png" width="100%" height="40%">


- open cluod shell

<img src="image\open cluod shell.png" width="100%" height="40%">
<img src="image\enter password.png" width="100%" height="40%">

- switch to the database called "demo"

<img src="image\database changed.png" width="75%" height="40%">

- sql commands can be executed; however, the output formatting is not very user-friendly since it is displayed in cloud shell

<img src="image\sql command.png" width="35%" height="40%">
<img src="image\sql displayed.png" width="100%" height="40%">
<img src="image\919 row.png" width="100%" height="40%">

- As the output formatting is not very user-friendly, we will use DBeaver instead

### Using DBeaver
- we will be able to connect to the public IP address of the respective cluster

<img src="image\DBeaver.png" width="100%" height="40%">

- the demo is kafka-class-db-001

<img src="image\demo.png" width="100%" height="40%">

- the demo is kafka-class-db-002

<img src="image\demo2.png" width="100%" height="40%">

---

## Step 2: Provision a GCP Compute Engine instance
### Create Compute Engine instance
<img src="image\VM.png" width="100%" height="40%">

### Using SSH Compute Engine

- lists files and directories
```sh
$ ls -lrt
```
<img src="image\ls -lrt.png" width="100%" height="40%">

- change the current working directory 
```sh
$ cd kafka-r2de-demo/
```
<img src="image\cd kafka-r2de-demo.png" width="75%" height="40%">

- lists files and directories in kafka-r2de-demo/
```sh
$ ls -lrt
```
<img src="image\ls in kafka-r2de-demo.png" width="100%" height="40%">

- start all containers to initialize the kafka cluster
```sh
$ docker compose up -d
```
<img src="image\docker compose up -d.png" width="100%" height="40%">

- list all docker containers, including both running and stopped ones
```sh
$ docker ps -a
```
<img src="image\docker ps -a.png" width="100%" height="40%">

- use kafka confluent control center

<img src="image\External IP address.png" width="100%" height="40%">
<img src="image\9021.png" width="100%" height="40%">
<img src="image\control center.png" width="100%" height="40%">
<img src="image\CONTROLCENTER.png" width="100%" height="40%">

---